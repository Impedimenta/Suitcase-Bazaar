Suitcase --name="Hexdump" --window-height="390" --window-width="670" \
--control-title="Drop a file here…" \
--control-type="dropped-files-label" \
--control-group-identifier="com.fr" \
--control-title="Dump" \
--control-type="button" \
--control-action="/usr/bin/hexdump" \
--control-action-parameter="-v,-n,255,-s,PAGE_VALUE,-C,SUITCASE_DROPPED_FILES" \
--control-action-destination="com.output.hexdump" \
--control-group-identifier="com.fr" \
--control-title=" " \
--control-type="text-mono" \
--control-identifier="com.output.hexdump" \
--control-type="spacer" \
--control-group-identifier="com.page" \
--control-type="button" \
--control-title="<" \
--control-group-identifier="com.page" \
--control-action="/bin/bash" \
--control-action-parameter="-c,echo \$((\$PAGE_VALUE - 128))" \
--control-action-destination="PAGE_VALUE" \
--control-type="label" \
--control-title="0" \
--control-identifier="PAGE_VALUE" \
--control-group-identifier="com.page" \
--control-type="button" \
--control-title=">" \
--control-group-identifier="com.page" \
--control-action="/bin/bash" \
--control-action-parameter="-c,echo \$((\$PAGE_VALUE + 128))" \
--control-action-destination="PAGE_VALUE"






hexdump -v -n 512 -C RSC-FORK.data