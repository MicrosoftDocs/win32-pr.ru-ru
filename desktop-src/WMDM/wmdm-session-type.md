---
title: Перечисление WMDM_SESSION_TYPE
description: Тип \_ перечисления типа сеанса вмдм \_ определяет тип сеанса.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694642"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="eef14-104">\_ \_ Перечисление типов сеансов вмдм</span><span class="sxs-lookup"><span data-stu-id="eef14-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="eef14-105">Тип перечисления типа **\_ сеанса вмдм \_** определяет тип сеанса.</span><span class="sxs-lookup"><span data-stu-id="eef14-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef14-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eef14-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="eef14-107">Константы</span><span class="sxs-lookup"><span data-stu-id="eef14-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eef14-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**ВМДМ \_ сеанс \_ нет**</span><span class="sxs-lookup"><span data-stu-id="eef14-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="eef14-109">Сеанс не определен.</span><span class="sxs-lookup"><span data-stu-id="eef14-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="eef14-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_Перенаправление сеанса вмдм \_ \_ на \_ устройство**</span><span class="sxs-lookup"><span data-stu-id="eef14-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="eef14-111">Сеанс определяется как передача данных на устройство.</span><span class="sxs-lookup"><span data-stu-id="eef14-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="eef14-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_Перемещение сеанса \_ вмдм \_ с \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="eef14-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="eef14-113">Сеанс определяется как передача данных с устройства.</span><span class="sxs-lookup"><span data-stu-id="eef14-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="eef14-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_Удаление сеанса \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="eef14-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="eef14-115">Сеанс определяется как удаление данных.</span><span class="sxs-lookup"><span data-stu-id="eef14-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="eef14-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_пользовательский сеанс \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="eef14-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="eef14-117">Сеанс определяется как пользовательский сеанс.</span><span class="sxs-lookup"><span data-stu-id="eef14-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eef14-118">Требования</span><span class="sxs-lookup"><span data-stu-id="eef14-118">Requirements</span></span>



| <span data-ttu-id="eef14-119">Требование</span><span class="sxs-lookup"><span data-stu-id="eef14-119">Requirement</span></span> | <span data-ttu-id="eef14-120">Значение</span><span class="sxs-lookup"><span data-stu-id="eef14-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eef14-121">Header</span><span class="sxs-lookup"><span data-stu-id="eef14-121">Header</span></span><br/> | <dl> <span data-ttu-id="eef14-122"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eef14-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef14-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eef14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef14-124">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="eef14-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





