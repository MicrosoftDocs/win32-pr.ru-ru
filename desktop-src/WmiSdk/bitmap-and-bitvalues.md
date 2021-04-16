---
description: — Это целое число, связанное со свойством с квалификаторами BitMap и Битвалуе.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Квалификаторы BitMap и Битвалуе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650668"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="1ac11-103">Квалификаторы BitMap и Битвалуе</span><span class="sxs-lookup"><span data-stu-id="1ac11-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="1ac11-104">Точечный рисунок — это целое число, связанное со свойством с квалификаторами **Bitmap** и **битвалуе** .</span><span class="sxs-lookup"><span data-stu-id="1ac11-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="1ac11-105">Каждый бит значения свойства выступает в качестве индекса в массиве значений в списке **битвалуе** .</span><span class="sxs-lookup"><span data-stu-id="1ac11-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="1ac11-106">Поскольку несколько битов в значении свойства могут одновременно иметь значение "on", можно использовать одно значение свойства для указания нескольких одновременных значений.</span><span class="sxs-lookup"><span data-stu-id="1ac11-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="1ac11-107">Например, следующий пример кода MOF устанавливает свойство **filetype** как квалификаторы **BitMap** и **битвалуес** .</span><span class="sxs-lookup"><span data-stu-id="1ac11-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="1ac11-108">Он дополнительно устанавливает, что бит низкого порядка (бит 0) соответствует значению "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="1ac11-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="1ac11-109">Следующий бит (бит 1) соответствует "Hidden" и т. д.</span><span class="sxs-lookup"><span data-stu-id="1ac11-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="1ac11-110">(Не все биты должны быть значительными.</span><span class="sxs-lookup"><span data-stu-id="1ac11-110">(Not all bits must be significant.</span></span> <span data-ttu-id="1ac11-111">В этой 8-разрядной системе два старших бита, 6 и 7, не имеют значимости.)</span><span class="sxs-lookup"><span data-stu-id="1ac11-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="1ac11-112">Если свойство **filetype** сообщает значение 7 (BITS 0000 0111), то файл имеет тип "только для чтения", "система" и "скрытый".</span><span class="sxs-lookup"><span data-stu-id="1ac11-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="1ac11-113">Если свойство **filetype** сообщает значение 18 (0x12, бит 0001 0010), это скрытый подкаталог.</span><span class="sxs-lookup"><span data-stu-id="1ac11-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="1ac11-114">Существует два разных типа точечных рисунков, использующих MOF-код:</span><span class="sxs-lookup"><span data-stu-id="1ac11-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="1ac11-115">Последовательные значащие биты, начинающиеся с младшего бита (бит 0)</span><span class="sxs-lookup"><span data-stu-id="1ac11-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="1ac11-116">Можно определить массив битовых значений без явного указания значимых битов, если значащие биты начинаются с младшего бита (бит 0) и выполняются вверх без перерыва с помощью всех элементов в массиве **битвалуе** .</span><span class="sxs-lookup"><span data-stu-id="1ac11-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="1ac11-117">В следующем примере кода MOF выполняется та же функция, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="1ac11-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="1ac11-118">Значащий бит предшествует незначащим битом</span><span class="sxs-lookup"><span data-stu-id="1ac11-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="1ac11-119">Если бит низкого порядка неважен или последовательность значащих битов не является непрерывной, необходимо указать оба квалификатора: **BitMap** и **битвалуес** .</span><span class="sxs-lookup"><span data-stu-id="1ac11-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="1ac11-120">В следующем примере кода MOF показана ситуация, в которой бит низкого порядка не важен и существует разрыв в последовательности значащих битов.</span><span class="sxs-lookup"><span data-stu-id="1ac11-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="1ac11-121">В этом случае Установка бита низкого порядка (бит 0) не имеет значения и игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1ac11-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="1ac11-122">Однако Установка бита 1 (0x2) означает, что это сообщение электронной почты помечено к исполнению, а Установка бита 4 (0x8) означает, что уведомление о доставке будет отправлено отправителю, когда сообщение поступило в почтовый ящик получателя, и если установить бит 5 (0x10), что уведомление о прочтении должно быть отправлено отправителю при открытии сообщения электронной почты получателем.</span><span class="sxs-lookup"><span data-stu-id="1ac11-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="1ac11-123">Установка всех трех значащих битов (0x1A) задает все три условия для сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1ac11-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac11-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ac11-124">Remarks</span></span>

<span data-ttu-id="1ac11-125">При принятии решения о том, следует ли использовать / Квалификаторы значений BitMap **битвалуес** или **ValueMap** /  , определите, может ли любое из указанных значений выполняться параллельно.</span><span class="sxs-lookup"><span data-stu-id="1ac11-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="1ac11-126">Если могут существовать несколько одновременных значений, необходимо использовать **BitMap** / **битвалуес**.</span><span class="sxs-lookup"><span data-stu-id="1ac11-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="1ac11-127">Если все значения являются взаимоисключающими, следует использовать  / Квалификаторы **значений** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="1ac11-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ac11-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1ac11-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac11-129">Квалификаторы ValueMap и value</span><span class="sxs-lookup"><span data-stu-id="1ac11-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



