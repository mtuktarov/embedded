```bash
keys=("Name" "Nickname" "AKA" "Occupation")
values=("Greta" "Eco warrior" "Captain Planet" "Unemployed")

matching_keys=()
matching_values=()

for i in $(seq 0 $((${#keys[@]} - 1))); do
  set -- ${values[$i]}
  word_count=$#
  if [ "$word_count" -eq 2 ]; then
    matching_keys+=("${keys[$i]}")
    matching_values+=("${values[$i]}")
  fi
done

for i in $(seq 0 $((${#matching_keys[@]} - 1))); do
  echo "${matching_keys[$i]} - ${matching_values[$i]}"
done

newObjModified=()

for value in "${values[@]}"; do
  newObjModified+=( $(echo "$value" | tr '[:lower:]' '[:upper:]') )
done

for i in "${!keys[@]}"; do
  echo "Original: ${keys[$i]}='${new_values[$i]}'"
done
```
