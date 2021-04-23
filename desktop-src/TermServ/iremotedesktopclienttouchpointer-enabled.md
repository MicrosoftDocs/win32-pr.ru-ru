---
title: Свойство Enabled Иремотедесктопклиенттаучпоинтер
description: Включена ли функция сенсорного указателя в клиентском элементе управления контейнера приложения RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Включенное свойство службы удаленных рабочих столов
- Включенное свойство службы удаленных рабочих столов, интерфейс Иремотедесктопклиенттаучпоинтер
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиенттаучпоинтер, включенное свойство
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681968"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="1f623-106">Свойство Иремотедесктопклиенттаучпоинтер:: Enabled</span><span class="sxs-lookup"><span data-stu-id="1f623-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="1f623-107">Включена ли функция сенсорного указателя в клиентском элементе управления контейнера приложения RDP.</span><span class="sxs-lookup"><span data-stu-id="1f623-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="1f623-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1f623-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f623-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f623-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="1f623-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f623-110">Property value</span></span>

<span data-ttu-id="1f623-111">**значение true** , если включена функция сенсорного указателя. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f623-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f623-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1f623-112">Requirements</span></span>



| <span data-ttu-id="1f623-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1f623-113">Requirement</span></span> | <span data-ttu-id="1f623-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1f623-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f623-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f623-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1f623-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1f623-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="1f623-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f623-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1f623-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f623-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="1f623-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1f623-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f623-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f623-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="1f623-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1f623-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f623-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f623-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="1f623-123">IID</span><span class="sxs-lookup"><span data-stu-id="1f623-123">IID</span></span><br/>                      | <span data-ttu-id="1f623-124">IID \_ иремотедесктопклиенттаучпоинтер определен как 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="1f623-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f623-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f623-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f623-126">**иремотедесктопклиенттаучпоинтер**</span><span class="sxs-lookup"><span data-stu-id="1f623-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

