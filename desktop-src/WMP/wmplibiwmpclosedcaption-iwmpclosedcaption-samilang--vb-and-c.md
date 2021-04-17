---
title: Ивмпклоседкаптион Самиланг, свойство
description: Свойство Самиланг получает или задает язык, отображаемый для скрытых субтитров.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Проигрыватель Windows Media для свойства Самиланг
- Самиланг свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Самиланг
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708548"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="b6f7d-106">Свойство Ивмпклоседкаптион:: Самиланг</span><span class="sxs-lookup"><span data-stu-id="b6f7d-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="b6f7d-107">Свойство **самиланг** получает или задает язык, отображаемый для скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f7d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6f7d-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="b6f7d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b6f7d-109">Property value</span></span>

<span data-ttu-id="b6f7d-110">**Строка System. String** , которая является именем, указанным в идентификаторе языка файла Sami.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f7d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6f7d-111">Remarks</span></span>

<span data-ttu-id="b6f7d-112">Файл SAMI может содержать текст для одного или нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="b6f7d-113">Языки, доступные для скрытых титров, определяются между тегами <STYLE> и </STYLE> в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="b6f7d-114">Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.).</span><span class="sxs-lookup"><span data-stu-id="b6f7d-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="b6f7d-115">Имя, указанное для языка, может быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="b6f7d-116">Например, для определения английского языка (США) можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b6f7d-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="b6f7d-117">Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="b6f7d-118">Строка, заданная с помощью **самиланг** , должна соответствовать атрибуту **Name** в описателе языка.</span><span class="sxs-lookup"><span data-stu-id="b6f7d-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f7d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b6f7d-119">Requirements</span></span>



| <span data-ttu-id="b6f7d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b6f7d-120">Requirement</span></span> | <span data-ttu-id="b6f7d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b6f7d-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f7d-122">Версия</span><span class="sxs-lookup"><span data-stu-id="b6f7d-122">Version</span></span><br/>   | <span data-ttu-id="b6f7d-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b6f7d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6f7d-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6f7d-124">Namespace</span></span><br/> | <span data-ttu-id="b6f7d-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b6f7d-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6f7d-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="b6f7d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6f7d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f7d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f7d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6f7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f7d-129">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="b6f7d-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="b6f7d-130">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f7d-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6f7d-131">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f7d-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





