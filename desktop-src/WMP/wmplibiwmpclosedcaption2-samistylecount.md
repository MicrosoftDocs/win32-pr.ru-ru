---
title: IWMPClosedCaption2 Самистилекаунт, свойство
description: Свойство Самистилекаунт возвращает количество стилей, поддерживаемых текущим файлом SAMI.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Проигрыватель Windows Media для свойства Самистилекаунт
- Самистилекаунт свойство проигрывателя Windows Media Player, интерфейс IWMPClosedCaption2
- Интерфейс IWMPClosedCaption2 Windows Media Player, свойство Самистилекаунт
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689314"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="eefdf-106">Свойство IWMPClosedCaption2:: Самистилекаунт</span><span class="sxs-lookup"><span data-stu-id="eefdf-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="eefdf-107">Свойство **самистилекаунт** возвращает количество стилей, поддерживаемых текущим файлом Sami.</span><span class="sxs-lookup"><span data-stu-id="eefdf-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefdf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eefdf-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="eefdf-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eefdf-109">Property value</span></span>

<span data-ttu-id="eefdf-110">Объект **System. Int32** , который является числом стилей.</span><span class="sxs-lookup"><span data-stu-id="eefdf-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefdf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eefdf-111">Remarks</span></span>

<span data-ttu-id="eefdf-112">Это свойство возвращает значение 0, если файл цифрового мультимедиа не открыт (Аксвиндовсмедиаплайер. Опенстате равен 13).</span><span class="sxs-lookup"><span data-stu-id="eefdf-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="eefdf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="eefdf-113">Requirements</span></span>



| <span data-ttu-id="eefdf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="eefdf-114">Requirement</span></span> | <span data-ttu-id="eefdf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="eefdf-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefdf-116">Версия</span><span class="sxs-lookup"><span data-stu-id="eefdf-116">Version</span></span><br/>   | <span data-ttu-id="eefdf-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="eefdf-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="eefdf-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eefdf-118">Namespace</span></span><br/> | <span data-ttu-id="eefdf-119">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="eefdf-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="eefdf-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="eefdf-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eefdf-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eefdf-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefdf-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eefdf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefdf-123">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="eefdf-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="eefdf-124">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="eefdf-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eefdf-125">**Ивмпклоседкаптион. Самистиле (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="eefdf-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eefdf-126">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="eefdf-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eefdf-127">**IWMPClosedCaption2. Жетсамистиленаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="eefdf-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





