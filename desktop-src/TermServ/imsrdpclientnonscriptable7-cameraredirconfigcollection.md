---
title: Свойство IMsRdpClientNonScriptable7 CameraRedirConfigCollection
description: Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Камераредирконфигколлектион
- Службы удаленных рабочих столов свойства Камераредирконфигколлектион, интерфейс IMsRdpClientNonScriptable7
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7, свойство Камераредирконфигколлектион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341395"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="7271f-106">Свойство IMsRdpClientNonScriptable7:: Камераредирконфигколлектион</span><span class="sxs-lookup"><span data-stu-id="7271f-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="7271f-107">Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="7271f-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="7271f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7271f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7271f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7271f-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="7271f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7271f-110">Property value</span></span>

<span data-ttu-id="7271f-111">Объект [имсрдпкамераредирконфигколлектион](imsrdpcameraredirconfigcollection.md) , представляющий коллекцию камер (и связанных конфигураций), которые доступны для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="7271f-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7271f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7271f-112">Requirements</span></span>

| <span data-ttu-id="7271f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7271f-113">Requirement</span></span> | <span data-ttu-id="7271f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7271f-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="7271f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7271f-115">Minimum supported client</span></span>| <span data-ttu-id="7271f-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="7271f-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="7271f-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7271f-117">Type library</span></span>            | <span data-ttu-id="7271f-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7271f-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="7271f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7271f-119">DLL</span></span>                  | <span data-ttu-id="7271f-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7271f-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="7271f-121">IID</span><span class="sxs-lookup"><span data-stu-id="7271f-121">IID</span></span>                      | <span data-ttu-id="7271f-122">IID \_ IMsRdpClientNonScriptable7 определен как 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="7271f-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="7271f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7271f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7271f-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="7271f-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>