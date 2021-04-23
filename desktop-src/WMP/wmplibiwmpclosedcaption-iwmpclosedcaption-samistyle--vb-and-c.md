---
title: Ивмпклоседкаптион Самистиле, свойство
description: Свойство Самистиле получает или задает стиль закрытых субтитров.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Проигрыватель Windows Media для свойства Самистиле
- Самистиле свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Самистиле
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649061"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="3f15b-106">Свойство Ивмпклоседкаптион:: Самистиле</span><span class="sxs-lookup"><span data-stu-id="3f15b-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="3f15b-107">Свойство **самистиле** получает или задает стиль закрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="3f15b-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f15b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f15b-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="3f15b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3f15b-109">Property value</span></span>

<span data-ttu-id="3f15b-110">**Строка System. String** , которая является именем, указанным в идентификаторе стиля файла Sami.</span><span class="sxs-lookup"><span data-stu-id="3f15b-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f15b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f15b-111">Remarks</span></span>

<span data-ttu-id="3f15b-112">Файл SAMI может содержать несколько определений стиля формата.</span><span class="sxs-lookup"><span data-stu-id="3f15b-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="3f15b-113">Стили SAMI определены между тегами <STYLE> и </STYLE> в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="3f15b-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="3f15b-114">Стиль определяется с помощью текстовой строки, предшествующей \# символу.</span><span class="sxs-lookup"><span data-stu-id="3f15b-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="3f15b-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="3f15b-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="3f15b-116">Указывает стиль, создающий определенный шрифт.</span><span class="sxs-lookup"><span data-stu-id="3f15b-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="3f15b-117">Если параметр SAMI не указан, по умолчанию используется первый стиль, определенный в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="3f15b-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f15b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3f15b-118">Requirements</span></span>



| <span data-ttu-id="3f15b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3f15b-119">Requirement</span></span> | <span data-ttu-id="3f15b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3f15b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f15b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="3f15b-121">Version</span></span><br/>   | <span data-ttu-id="3f15b-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3f15b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3f15b-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3f15b-123">Namespace</span></span><br/> | <span data-ttu-id="3f15b-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3f15b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3f15b-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="3f15b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3f15b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3f15b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f15b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f15b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f15b-128">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="3f15b-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="3f15b-129">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f15b-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f15b-130">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f15b-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





