Suitcase --name="iOS Icon" \
--control-title="Drop Icon file here, it should be 1024 x 1024" \
	--control-type="dropped-files-label" \
--control-title="~/Desktop" \
    --control-type="text-field" \
    --control-identifier="OUTPUT_DIR" \
--control-title="Create" \
	--control-type="button" \
	--control-action="/bin/bash" --control-action-parameter="-cx,for sz in 1024 20 40 60 180 120 76 152 29 58 87 80 167; do sips -z \$sz \$sz \"\$SUITCASE_DROPPED_FILES\" --out \"\$OUTPUT_DIR/Icon-\$sz.png\"; done" \
	--control-title="error-text" \
	--control-type="error-text"
	
	
	
	
	
	--control-action="/bin/bash" --control-action-parameter="-cx,sips -z 1024 1024 \"$SUITCASE_DROPPED_FILES\" --out \"\$OUTPUT_DIR/Icon-1024.png\"" \


	--control-action="/bin/bash" --control-action-parameter="-cx,for sz in 1024 20; do sips -z $sz $sz \"$SUITCASE_DROPPED_FILES\" --out \"\$OUTPUT_DIR/Icon-$sz.png\"; done" \
