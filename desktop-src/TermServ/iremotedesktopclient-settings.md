---
title: Иремотедесктопклиент Settings, свойство
description: Извлекает объект параметров для клиента контейнера приложения протокол удаленного рабочего стола (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Свойства параметров службы удаленных рабочих столов
- Свойство параметров службы удаленных рабочих столов, интерфейс Иремотедесктопклиент
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиент, свойство Settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988939"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="0433c-106">Свойство Иремотедесктопклиент:: Settings</span><span class="sxs-lookup"><span data-stu-id="0433c-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="0433c-107">Извлекает объект параметров для клиента контейнера приложения протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="0433c-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="0433c-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0433c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0433c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0433c-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="0433c-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0433c-110">Property value</span></span>

<span data-ttu-id="0433c-111">Объект параметров для клиента RDP.</span><span class="sxs-lookup"><span data-stu-id="0433c-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="0433c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0433c-112">Requirements</span></span>



| <span data-ttu-id="0433c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0433c-113">Requirement</span></span> | <span data-ttu-id="0433c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0433c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0433c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0433c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0433c-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0433c-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="0433c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0433c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0433c-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0433c-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="0433c-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0433c-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0433c-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0433c-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="0433c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0433c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0433c-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0433c-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="0433c-123">IID</span><span class="sxs-lookup"><span data-stu-id="0433c-123">IID</span></span><br/>                      | <span data-ttu-id="0433c-124">IID \_ иремотедесктопклиент определен как 57D25668-625A-4905-BE4E-304CAA13F89C</span><span class="sxs-lookup"><span data-stu-id="0433c-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0433c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0433c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0433c-126">**иремотедесктопклиент**</span><span class="sxs-lookup"><span data-stu-id="0433c-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

