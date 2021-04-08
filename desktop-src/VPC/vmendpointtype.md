---
title: Перечисление Вмендпоинттипе (Впккоминтерфацес. h)
description: Указывает тип конечной точки.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- Перечисление Вмендпоинттипе Virtual PC
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891861"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="5fea4-104">Перечисление Вмендпоинттипе</span><span class="sxs-lookup"><span data-stu-id="5fea4-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="5fea4-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5fea4-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5fea4-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5fea4-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5fea4-107">Указывает тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5fea4-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fea4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fea4-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="5fea4-109">Константы</span><span class="sxs-lookup"><span data-stu-id="5fea4-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5fea4-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**Вмендпоинт \_ помощью канала NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="5fea4-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="5fea4-111">Сторона размещения.</span><span class="sxs-lookup"><span data-stu-id="5fea4-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="5fea4-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**Вмендпоинт \_ tcpip**</span><span class="sxs-lookup"><span data-stu-id="5fea4-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="5fea4-113">Сторона виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5fea4-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fea4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5fea4-114">Requirements</span></span>



| <span data-ttu-id="5fea4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5fea4-115">Requirement</span></span> | <span data-ttu-id="5fea4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5fea4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fea4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fea4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5fea4-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5fea4-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fea4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fea4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5fea4-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5fea4-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5fea4-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5fea4-121">End of client support</span></span><br/>    | <span data-ttu-id="5fea4-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5fea4-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5fea4-123">Продукт</span><span class="sxs-lookup"><span data-stu-id="5fea4-123">Product</span></span><br/>                  | <span data-ttu-id="5fea4-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5fea4-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5fea4-125">Header</span><span class="sxs-lookup"><span data-stu-id="5fea4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fea4-126"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fea4-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fea4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fea4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fea4-128">**Ивмвиртуалмачине:: Старткоммуникатиончаннел**</span><span class="sxs-lookup"><span data-stu-id="5fea4-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

