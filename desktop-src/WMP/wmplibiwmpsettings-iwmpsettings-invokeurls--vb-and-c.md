---
title: Ивмпсеттингс Инвокеурлс, свойство
description: Свойство Инвокеурлс получает или задает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Проигрыватель Windows Media для свойства Инвокеурлс
- Инвокеурлс свойство проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Инвокеурлс
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718176"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="85fee-106">Свойство Ивмпсеттингс:: Инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="85fee-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="85fee-107">Свойство **инвокеурлс** получает или задает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="85fee-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="85fee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85fee-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="85fee-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="85fee-109">Property value</span></span>

<span data-ttu-id="85fee-110">Значение **System. Boolean** , указывающее, должны ли события URL запускаться в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="85fee-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="85fee-111">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="85fee-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="85fee-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85fee-112">Remarks</span></span>

<span data-ttu-id="85fee-113">Цифровые файлы мультимедиа и потоки могут содержать команды сценария URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="85fee-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="85fee-114">При отправке команды скрипта URL-адреса элементу управления проигрывателя Windows Media он сначала передается обработчику событий **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** независимо от значения, полученного **инвокеурлс**.</span><span class="sxs-lookup"><span data-stu-id="85fee-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="85fee-115">После выхода **\_ Вмпокксевентс \_ Скрипткоммандевент** проигрыватель Windows Media проверяет **инвокеурлс** , чтобы определить, следует ли запускать веб-браузер по умолчанию с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="85fee-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="85fee-116">Вы можете выборочно отображать URL-адреса, проверив их в **\_ вмпокксевентс \_ скрипткоммандевент** и установив нужные **инвокеурлс** .</span><span class="sxs-lookup"><span data-stu-id="85fee-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="85fee-117">Требования</span><span class="sxs-lookup"><span data-stu-id="85fee-117">Requirements</span></span>



| <span data-ttu-id="85fee-118">Требование</span><span class="sxs-lookup"><span data-stu-id="85fee-118">Requirement</span></span> | <span data-ttu-id="85fee-119">Значение</span><span class="sxs-lookup"><span data-stu-id="85fee-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fee-120">Версия</span><span class="sxs-lookup"><span data-stu-id="85fee-120">Version</span></span><br/>   | <span data-ttu-id="85fee-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="85fee-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="85fee-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="85fee-122">Namespace</span></span><br/> | <span data-ttu-id="85fee-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="85fee-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="85fee-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="85fee-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="85fee-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="85fee-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85fee-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85fee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85fee-127">**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="85fee-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="85fee-128">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="85fee-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





