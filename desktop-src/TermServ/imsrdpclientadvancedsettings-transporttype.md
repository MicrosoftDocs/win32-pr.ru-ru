---
title: Имсрдпклиентадванцедсеттингс TransportType, свойство
description: Указывает тип транспорта, используемый клиентом.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportType
- Службы удаленных рабочих столов свойства TransportType, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672465"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="d3ad1-106">Свойство Имсрдпклиентадванцедсеттингс:: TransportType</span><span class="sxs-lookup"><span data-stu-id="d3ad1-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="d3ad1-107">Указывает тип транспорта, используемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="d3ad1-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="d3ad1-108">Это свойство не используется удаленный рабочий стол элементом управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d3ad1-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="d3ad1-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d3ad1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ad1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3ad1-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="d3ad1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d3ad1-111">Property value</span></span>

<span data-ttu-id="d3ad1-112">Задает тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="d3ad1-112">Sets the transport type.</span></span> <span data-ttu-id="d3ad1-113">Этот метод может быть выполнен, но набор значений никогда не используется элементом управления удаленный рабочий стол ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d3ad1-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ad1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3ad1-114">Remarks</span></span>

<span data-ttu-id="d3ad1-115">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d3ad1-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ad1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d3ad1-116">Requirements</span></span>



| <span data-ttu-id="d3ad1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d3ad1-117">Requirement</span></span> | <span data-ttu-id="d3ad1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d3ad1-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ad1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3ad1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ad1-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3ad1-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d3ad1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3ad1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ad1-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3ad1-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d3ad1-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d3ad1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3ad1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad1-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d3ad1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ad1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ad1-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad1-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d3ad1-127">IID</span><span class="sxs-lookup"><span data-stu-id="d3ad1-127">IID</span></span><br/>                      | <span data-ttu-id="d3ad1-128">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d3ad1-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3ad1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3ad1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ad1-130">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d3ad1-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





