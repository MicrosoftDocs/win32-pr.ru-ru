---
title: IMsRdpClientSecuredSettings2 ПКБ, свойство
description: Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер. | IMsRdpClientSecuredSettings2 ПКБ, свойство
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientSecuredSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientSecuredSettings2, свойство ПКБ
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674657"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="8af87-107">IMsRdpClientSecuredSettings2::P свойство CB</span><span class="sxs-lookup"><span data-stu-id="8af87-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="8af87-108">Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="8af87-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="8af87-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8af87-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af87-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8af87-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="8af87-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8af87-111">Property value</span></span>

<span data-ttu-id="8af87-112">Параметр ПКБ.</span><span class="sxs-lookup"><span data-stu-id="8af87-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af87-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8af87-113">Requirements</span></span>



| <span data-ttu-id="8af87-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8af87-114">Requirement</span></span> | <span data-ttu-id="8af87-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8af87-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8af87-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8af87-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8af87-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8af87-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="8af87-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8af87-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8af87-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8af87-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8af87-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8af87-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="8af87-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af87-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8af87-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8af87-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8af87-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af87-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af87-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8af87-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af87-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="8af87-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





