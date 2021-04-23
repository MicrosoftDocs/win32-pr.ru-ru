---
title: IMsRdpClientAdvancedSettings8 Клиентпротоколспек, свойство
description: Указывает протокол удаленного рабочего стола, используемый между клиентом и сервером.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клиентпротоколспек
- Службы удаленных рабочих столов свойства Клиентпротоколспек, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Клиентпротоколспек
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988340"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="6174d-106">Свойство IMsRdpClientAdvancedSettings8:: Клиентпротоколспек</span><span class="sxs-lookup"><span data-stu-id="6174d-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="6174d-107">Указывает протокол удаленного рабочего стола, используемый между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6174d-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="6174d-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6174d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6174d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6174d-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="6174d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6174d-110">Property value</span></span>

<span data-ttu-id="6174d-111">Значение перечисления [**клиентспек**](clientspec.md) , указывающее протокол удаленного рабочего стола, используемый между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6174d-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="6174d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6174d-112">Requirements</span></span>



| <span data-ttu-id="6174d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6174d-113">Requirement</span></span> | <span data-ttu-id="6174d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6174d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6174d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6174d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6174d-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6174d-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="6174d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6174d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6174d-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6174d-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="6174d-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6174d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6174d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6174d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6174d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6174d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6174d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6174d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6174d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6174d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6174d-124">**клиентспек**</span><span class="sxs-lookup"><span data-stu-id="6174d-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="6174d-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6174d-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





