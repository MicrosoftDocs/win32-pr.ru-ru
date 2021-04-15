---
title: IWMPClosedCaption2 Самилангкаунт, свойство
description: Свойство Самилангкаунт возвращает количество языков, поддерживаемых текущим файлом SAMI.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Проигрыватель Windows Media для свойства Самилангкаунт
- Самилангкаунт свойство проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, свойство Самилангкаунт
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689316"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="f5f71-106">Свойство IWMPClosedCaption2:: Самилангкаунт</span><span class="sxs-lookup"><span data-stu-id="f5f71-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="f5f71-107">Свойство **самилангкаунт** возвращает количество языков, поддерживаемых текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="f5f71-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f71-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f71-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f5f71-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f5f71-109">Property value</span></span>

<span data-ttu-id="f5f71-110">Значение **System. Int32** , которое является числом поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="f5f71-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f71-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5f71-111">Remarks</span></span>

<span data-ttu-id="f5f71-112">Это свойство возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).</span><span class="sxs-lookup"><span data-stu-id="f5f71-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f71-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5f71-113">Requirements</span></span>



| <span data-ttu-id="f5f71-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5f71-114">Requirement</span></span> | <span data-ttu-id="f5f71-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5f71-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f71-116">Версия</span><span class="sxs-lookup"><span data-stu-id="f5f71-116">Version</span></span><br/>   | <span data-ttu-id="f5f71-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f5f71-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f5f71-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5f71-118">Namespace</span></span><br/> | <span data-ttu-id="f5f71-119">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f5f71-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f5f71-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="f5f71-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f5f71-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f71-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f71-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5f71-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f71-123">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="f5f71-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f5f71-124">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f5f71-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5f71-125">**Ивмпклоседкаптион. Самиланг (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f5f71-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5f71-126">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f5f71-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5f71-127">**IWMPClosedCaption2. Жетсамилангнаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f5f71-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





