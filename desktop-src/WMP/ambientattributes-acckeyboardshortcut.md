---
title: Амбиентаттрибутес. Акккэйбоардшорткут
description: Атрибут Акккэйбоардшорткут указывает или получает описание сочетания клавиш для любого элемента.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Акккэйбоардшорткут
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694883"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="70c21-104">Амбиентаттрибутес. Акккэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="70c21-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="70c21-105">Атрибут **акккэйбоардшорткут** указывает или получает описание сочетания клавиш для любого элемента.</span><span class="sxs-lookup"><span data-stu-id="70c21-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="70c21-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="70c21-106">Possible Values</span></span>

<span data-ttu-id="70c21-107">Этот атрибут является **строкой** для чтения и записи со значением по умолчанию "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="70c21-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="70c21-108">Для элемента **Button** этот атрибут имеет значение по умолчанию "пробел" или "Ввод".</span><span class="sxs-lookup"><span data-stu-id="70c21-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="70c21-109">Для элемента **Slider** по умолчанию используется значение «стрелка вправо/вверх для увеличения, стрелка влево или вниз для уменьшения».</span><span class="sxs-lookup"><span data-stu-id="70c21-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="70c21-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70c21-110">Remarks</span></span>

<span data-ttu-id="70c21-111">Этот атрибут используется в целях обеспечения специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="70c21-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="70c21-112">Это позволяет программе чтения просматривать вслух сочетания клавиш для любого элемента.</span><span class="sxs-lookup"><span data-stu-id="70c21-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="70c21-113">Этот атрибут не задает ярлык.</span><span class="sxs-lookup"><span data-stu-id="70c21-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="70c21-114">Scripter должен выполнить эту работу.</span><span class="sxs-lookup"><span data-stu-id="70c21-114">The scripter must do that work.</span></span>

<span data-ttu-id="70c21-115">Этот атрибут также применяется к элементам кнопки внутри элемента управления группы кнопок.</span><span class="sxs-lookup"><span data-stu-id="70c21-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c21-116">Требования</span><span class="sxs-lookup"><span data-stu-id="70c21-116">Requirements</span></span>



| <span data-ttu-id="70c21-117">Требование</span><span class="sxs-lookup"><span data-stu-id="70c21-117">Requirement</span></span> | <span data-ttu-id="70c21-118">Значение</span><span class="sxs-lookup"><span data-stu-id="70c21-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="70c21-119">Версия</span><span class="sxs-lookup"><span data-stu-id="70c21-119">Version</span></span><br/> | <span data-ttu-id="70c21-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="70c21-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70c21-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70c21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c21-122">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="70c21-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





