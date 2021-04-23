---
description: Указывает отношение наследования для службы.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: Перечисление WPD_SERVICE_INHERITANCE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704159"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="96678-103">\_ \_ Перечисление типов наследования службы WPD \_</span><span class="sxs-lookup"><span data-stu-id="96678-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="96678-104">Тип **перечисления \_ \_ \_ типов наследования службы WPD** указывает отношение наследования для службы.</span><span class="sxs-lookup"><span data-stu-id="96678-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="96678-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96678-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="96678-106">Константы</span><span class="sxs-lookup"><span data-stu-id="96678-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96678-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_ \_ Реализация наследования службы WPD \_**</span><span class="sxs-lookup"><span data-stu-id="96678-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="96678-108">Служба наследует реализацию абстрактного определения службы.</span><span class="sxs-lookup"><span data-stu-id="96678-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96678-109">Требования</span><span class="sxs-lookup"><span data-stu-id="96678-109">Requirements</span></span>



| <span data-ttu-id="96678-110">Требование</span><span class="sxs-lookup"><span data-stu-id="96678-110">Requirement</span></span> | <span data-ttu-id="96678-111">Значение</span><span class="sxs-lookup"><span data-stu-id="96678-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="96678-112">Header</span><span class="sxs-lookup"><span data-stu-id="96678-112">Header</span></span><br/> | <dl> <span data-ttu-id="96678-113"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="96678-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96678-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96678-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96678-115">**Ипортабледевицесервицекапабилитиес:: Жетинхеритедсервицес**</span><span class="sxs-lookup"><span data-stu-id="96678-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




