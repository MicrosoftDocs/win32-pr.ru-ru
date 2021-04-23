---
title: IWMPSettings2 Дефаултаудиолангуаже, свойство
description: Свойство Дефаултаудиолангуаже получает код локали (LCID) используемого по умолчанию звукового языка, указанного в проигрывателе Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Проигрыватель Windows Media для свойства Дефаултаудиолангуаже
- Дефаултаудиолангуаже свойство проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, свойство Дефаултаудиолангуаже
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685442"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="71e5b-106">IWMPSettings2: свойство Ефаултаудиолангуаже:d</span><span class="sxs-lookup"><span data-stu-id="71e5b-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="71e5b-107">Свойство **дефаултаудиолангуаже** получает код локали (LCID) используемого по умолчанию звукового языка, указанного в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="71e5b-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="71e5b-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="71e5b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e5b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71e5b-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="71e5b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="71e5b-110">Property value</span></span>

<span data-ttu-id="71e5b-111">Значение **System. Int32** , которое является LCID.</span><span class="sxs-lookup"><span data-stu-id="71e5b-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e5b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71e5b-112">Remarks</span></span>

<span data-ttu-id="71e5b-113">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="71e5b-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e5b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="71e5b-114">Requirements</span></span>



| <span data-ttu-id="71e5b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="71e5b-115">Requirement</span></span> | <span data-ttu-id="71e5b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="71e5b-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e5b-117">Версия</span><span class="sxs-lookup"><span data-stu-id="71e5b-117">Version</span></span><br/>   | <span data-ttu-id="71e5b-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="71e5b-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="71e5b-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71e5b-119">Namespace</span></span><br/> | <span data-ttu-id="71e5b-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="71e5b-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="71e5b-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="71e5b-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="71e5b-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="71e5b-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e5b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71e5b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e5b-124">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71e5b-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71e5b-125">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71e5b-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="71e5b-126">**Интерфейс IWMPSettings2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="71e5b-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





