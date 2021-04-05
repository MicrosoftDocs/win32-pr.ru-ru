---
title: Свойство IMsRdpClientNonScriptable7 Clipboard
description: Возвращает контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства буфера обмена
- Свойство буфера обмена службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable7
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7, свойство Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "103989876"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="64dcc-106">Свойство IMsRdpClientNonScriptable7:: Clipboard</span><span class="sxs-lookup"><span data-stu-id="64dcc-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="64dcc-107">Возвращает контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="64dcc-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="64dcc-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="64dcc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="64dcc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64dcc-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="64dcc-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="64dcc-110">Property value</span></span>

<span data-ttu-id="64dcc-111">[Имсрдпклипбоард](imsrdpclipboard.md) , представляющий контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена (т. е. свойству [мануалклипбоардсинценаблед](imsrdpextendedsettings-property.md) присвоено значение **true**).</span><span class="sxs-lookup"><span data-stu-id="64dcc-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="64dcc-112">Требования</span><span class="sxs-lookup"><span data-stu-id="64dcc-112">Requirements</span></span>

| <span data-ttu-id="64dcc-113">Требование</span><span class="sxs-lookup"><span data-stu-id="64dcc-113">Requirement</span></span> | <span data-ttu-id="64dcc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="64dcc-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="64dcc-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64dcc-115">Minimum supported client</span></span>| <span data-ttu-id="64dcc-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="64dcc-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="64dcc-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="64dcc-117">Type library</span></span>            | <span data-ttu-id="64dcc-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="64dcc-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="64dcc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="64dcc-119">DLL</span></span>                  | <span data-ttu-id="64dcc-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="64dcc-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="64dcc-121">IID</span><span class="sxs-lookup"><span data-stu-id="64dcc-121">IID</span></span>                      | <span data-ttu-id="64dcc-122">IID \_ IMsRdpClientNonScriptable7 определен как 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="64dcc-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="64dcc-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64dcc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64dcc-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="64dcc-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>