# Remove Element

**Algorithm: Two Pointers (Два указателя)**

### ✅ Шаг 1: Уточнение задачи и ограничений

**English:**
We need to remove all occurrences of `val` from the array in-place. The first `k` elements must contain all values that are not equal to `val`. The order of the remaining elements does not matter, and elements after `k` are ignored.

**Русский:**
Нужно удалить все вхождения `val` из массива без создания нового массива. Первые `k` элементов должны содержать все значения, которые не равны `val`. Их порядок может измениться, а элементы после `k` не имеют значения.

`in-place` читается как **«ин плейс»** и означает изменение исходного массива без создания отдельного массива для результата.

`k` читается как **«кей»** и обозначает количество элементов, которые нужно оставить.

### ✅ Шаг 2: Выбор подхода и обоснование

**English:**
We use two pointers. `right` scans every element of the array, while `left` points to the position where the next valid element should be written. When `nums[right]` is not equal to `val`, we copy it to `nums[left]` and move `left` forward.

**Русский:**
Используем два указателя. `right` проходит по всем элементам массива, а `left` указывает на позицию, куда нужно записать следующий подходящий элемент. Если `nums[right]` не равно `val`, записываем этот элемент в `nums[left]` и сдвигаем `left` на одну позицию.

`right` читается как **«райт»**, `left` как **«лефт»**.

`nums[right]` читается примерно как **«намз райт»** и означает элемент массива `nums` с индексом `right`.

`nums[left]` читается как **«намз лефт»** и означает элемент массива `nums` с индексом `left`.

`!=` в Python читается как **«нот иквэл»**, то есть «не равно».

`!==` в TypeScript читается как **«нот иквэл иквэл»**, то есть строго «не равно».

### ✅ Шаг 3: Описание алгоритма

**English:**
Start with `left = 0`. Move `right` from the first element to the last one. If `nums[right] != val`, write `nums[right]` to `nums[left]` and increment `left`. At the end, `left` is the number of elements that are not equal to `val`, so we return it.

**Русский:**
Начинаем с `left = 0`. Указатель `right` проходит массив от первого элемента до последнего. Если текущий элемент не равен `val`, записываем его в позицию `left` и увеличиваем `left`. В конце `left` содержит количество элементов, которые не равны `val`, поэтому возвращаем его.

`left = 0` читается как **«лефт иквэл зиро»**.

`right = 0` читается как **«райт иквэл зиро»**.

`left += 1` читается как **«лефт плюс иквэл ван»** и означает увеличение `left` на единицу.

`nums[left] = nums[right]` читается как **«намз лефт иквэлз намз райт»**. Это означает, что элемент массива `nums` с индексом `left` становится равен элементу `nums` с индексом `right`.

Важно, что элементы не удаляются физически из массива. Подходящие значения просто сжимаются в его начало. Например, из `[3, 2, 2, 3]` после обработки первые два элемента становятся `[2, 2]`, а возвращаемое значение равно `2`. Остальная часть массива не проверяется.

### ✅ Шаг 4: Анализ сложности и крайних случаев

**English:**
We scan the array once, so the time complexity is `O(n)` (pronounced: "big O of n"). We use only two variables, so the extra space complexity is `O(1)` (pronounced: "big O of one"). The algorithm also works for an empty array because `range(len(nums))` performs zero iterations and `left` remains `0`.

**Русский:**
Мы проходим массив один раз, поэтому временная сложность составляет `O(n)` (читается: **«О большое от эн»**). Используются только два указателя, поэтому дополнительная сложность по памяти составляет `O(1)` (читается: **«О большое от единицы»**). Алгоритм также работает для пустого массива: цикл не выполнится ни разу, а `left` останется равен `0`.

`O(n)` читается по-английски как **«оу оф эн»** или полнее **«биг оу оф эн»**.

`O(1)` читается как **«оу оф ван»** или **«биг оу оф ван»**.
