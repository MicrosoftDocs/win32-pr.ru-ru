---
description: 'Дополнительные сведения: структура JET_TUPLELIMITS'
title: Структура JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999623"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="1b9fe-103">Структура JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="1b9fe-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="1b9fe-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1b9fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="1b9fe-105">Структура JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="1b9fe-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="1b9fe-106">Структура **JET_TUPLELIMITS** позволяет настраивать характеристики индекса кортежа для каждого индекса, а не для каждого экземпляра, с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="1b9fe-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="1b9fe-107">**Windows Server 2003:** Структура **JET_TUPLELIMITS** появилась в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="1b9fe-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1b9fe-108">Members</span></span>

<span data-ttu-id="1b9fe-109">**членгсмин**</span><span class="sxs-lookup"><span data-stu-id="1b9fe-109">**chLengthMin**</span></span>

<span data-ttu-id="1b9fe-110">Минимальная длина кортежа.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-110">The minimum length of a tuple.</span></span> <span data-ttu-id="1b9fe-111">Значение по умолчанию равно 3.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-111">The default value is 3.</span></span>

<span data-ttu-id="1b9fe-112">**членгсмакс**</span><span class="sxs-lookup"><span data-stu-id="1b9fe-112">**chLengthMax**</span></span>

<span data-ttu-id="1b9fe-113">Максимальная длина кортежа.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-113">The maximum length of a tuple.</span></span> <span data-ttu-id="1b9fe-114">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-114">The default value is 10.</span></span>

<span data-ttu-id="1b9fe-115">**чтоиндексмакс**</span><span class="sxs-lookup"><span data-stu-id="1b9fe-115">**chToIndexMax**</span></span>

<span data-ttu-id="1b9fe-116">Максимальная длина строки для индексирования.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-116">The maximum length of a string to index.</span></span> <span data-ttu-id="1b9fe-117">Например, если столбец имеет длину 100 символов, а **чтоиндексмакс** имеет значение 60, то будут индексироваться только первые 60 символов столбца.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="1b9fe-118">Значение по умолчанию — 32767.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-118">The default value is 32767.</span></span>

<span data-ttu-id="1b9fe-119">**кчинкремент**</span><span class="sxs-lookup"><span data-stu-id="1b9fe-119">**cchIncrement**</span></span>

<span data-ttu-id="1b9fe-120">Это позволяет настроить шаг на основе каждого индекса.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="1b9fe-121">**Windows Vista:** Член **кчинкремент** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="1b9fe-122">До Windows Vista объем смещения окна ("шаг") всегда равен 1, как показано в примере в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="1b9fe-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="1b9fe-123">**ичстарт**</span><span class="sxs-lookup"><span data-stu-id="1b9fe-123">**ichStart**</span></span>

<span data-ttu-id="1b9fe-124">Смещение в значении, с которого начинается извлечение кортежей из значения.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="1b9fe-125">**Windows Vista:** Член **ичстарт** появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="1b9fe-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b9fe-126">Remarks</span></span>

<span data-ttu-id="1b9fe-127">Индекс кортежа просматривает строку и индексирует все возможные подстроки **членгсмакс**.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="1b9fe-128">В конце строки (или в позиции **чтоиндексмакс** в зависимости от того, что происходит раньше), подстроки по меньшей мере **членгсмин** будут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="1b9fe-129">Индекс кортежа можно использовать для поиска строк с подстановочными знаками в начале и в конце.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="1b9fe-130">Если предположить, что строка с текстовым полем "дождя IN Испания \! " создается с параметрами **членгсмин**= 2, а **членгсмакс**= 3, в индексе создаются следующие записи:</span><span class="sxs-lookup"><span data-stu-id="1b9fe-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="1b9fe-131">ЧИАНГРАЙ</span><span class="sxs-lookup"><span data-stu-id="1b9fe-131">"RAI"</span></span>  
<span data-ttu-id="1b9fe-132">ЗНАЧЕНИЯ ТИПАНА</span><span class="sxs-lookup"><span data-stu-id="1b9fe-132">"AIN"</span></span>  
<span data-ttu-id="1b9fe-133">ОКНЕ</span><span class="sxs-lookup"><span data-stu-id="1b9fe-133">"IN "</span></span>  
<span data-ttu-id="1b9fe-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="1b9fe-134">"N I"</span></span>  
<span data-ttu-id="1b9fe-135">ОКНЕ</span><span class="sxs-lookup"><span data-stu-id="1b9fe-135">" IN"</span></span>  
<span data-ttu-id="1b9fe-136">ОКНЕ</span><span class="sxs-lookup"><span data-stu-id="1b9fe-136">"IN "</span></span>  
<span data-ttu-id="1b9fe-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="1b9fe-137">"N S"</span></span>  
<span data-ttu-id="1b9fe-138">ПОРТОВ</span><span class="sxs-lookup"><span data-stu-id="1b9fe-138">" SP"</span></span>  
<span data-ttu-id="1b9fe-139">SPA</span><span class="sxs-lookup"><span data-stu-id="1b9fe-139">"SPA"</span></span>  
<span data-ttu-id="1b9fe-140">"Паи"</span><span class="sxs-lookup"><span data-stu-id="1b9fe-140">"PAI"</span></span>  
<span data-ttu-id="1b9fe-141">ЗНАЧЕНИЯ ТИПАНА</span><span class="sxs-lookup"><span data-stu-id="1b9fe-141">"AIN"</span></span>  
<span data-ttu-id="1b9fe-142">"В \! "</span><span class="sxs-lookup"><span data-stu-id="1b9fe-142">"IN\!"</span></span>  
<span data-ttu-id="1b9fe-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="1b9fe-143">"N\!"</span></span>

<span data-ttu-id="1b9fe-144">Обратите внимание, что "IN" встречается дважды и что последняя запись ("N \! ") короче 3 (**членгсмакс**).</span><span class="sxs-lookup"><span data-stu-id="1b9fe-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="1b9fe-145">Также обратите внимание, что алгоритм разбиения не знает о пробелах или словах и обрабатывает все символы одинаково.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="1b9fe-146">**Windows XP:** Windows XP поддерживает индексы кортежей, но не имеет **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="1b9fe-147">Ядро СУБД будет использовать значения по умолчанию (**членгсмин**= 3, **членгсмакс**= 10, **чтоиндексмакс**= 32767).</span><span class="sxs-lookup"><span data-stu-id="1b9fe-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="1b9fe-148">Эти значения по-прежнему можно изменить, но они задаются для каждого экземпляра с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)и [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1b9fe-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="1b9fe-149">Требования</span><span class="sxs-lookup"><span data-stu-id="1b9fe-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b9fe-150"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1b9fe-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9fe-151">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9fe-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1b9fe-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9fe-153">Требуется Windows Server 2008, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9fe-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1b9fe-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9fe-155">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1b9fe-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1b9fe-156">См. также:</span><span class="sxs-lookup"><span data-stu-id="1b9fe-156">See Also</span></span>

[<span data-ttu-id="1b9fe-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="1b9fe-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="1b9fe-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1b9fe-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="1b9fe-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="1b9fe-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="1b9fe-160">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="1b9fe-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
