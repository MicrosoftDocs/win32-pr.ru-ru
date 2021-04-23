---
description: Определяет тип узла для вызывающего WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Перечисление WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538345"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="edb54-103">\_ \_ Перечисление идентификаторов узлов WLDP</span><span class="sxs-lookup"><span data-stu-id="edb54-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="edb54-104">Определяет тип узла для вызывающего WLDP.</span><span class="sxs-lookup"><span data-stu-id="edb54-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edb54-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="edb54-106">Константы</span><span class="sxs-lookup"><span data-stu-id="edb54-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="edb54-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ \_неизвестный \_ идентификатор узла**</span><span class="sxs-lookup"><span data-stu-id="edb54-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="edb54-108">Неизвестный тип узла.</span><span class="sxs-lookup"><span data-stu-id="edb54-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_ \_ глобальный идентификатор узла**</span><span class="sxs-lookup"><span data-stu-id="edb54-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-110">Тип узла — Глобальная политика.</span><span class="sxs-lookup"><span data-stu-id="edb54-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**\_код узла \_ WLDP \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="edb54-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-112">Тип узла — VBScript.</span><span class="sxs-lookup"><span data-stu-id="edb54-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_идентификатор узла \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="edb54-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-114">Тип узла — сервер сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="edb54-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_идентификатор узла \_ POWERSHELL**</span><span class="sxs-lookup"><span data-stu-id="edb54-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-116">Тип узла — Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="edb54-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_идентификатор узла \_ IE**</span><span class="sxs-lookup"><span data-stu-id="edb54-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-118">Тип узла — Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="edb54-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_идентификатор узла \_ MSI**</span><span class="sxs-lookup"><span data-stu-id="edb54-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="edb54-120">Тип узла — установщик Windows Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="edb54-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="edb54-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ \_ максимальный идентификатор узла**</span><span class="sxs-lookup"><span data-stu-id="edb54-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="edb54-122">Максимальное значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="edb54-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edb54-123">Требования</span><span class="sxs-lookup"><span data-stu-id="edb54-123">Requirements</span></span>



| <span data-ttu-id="edb54-124">Требование</span><span class="sxs-lookup"><span data-stu-id="edb54-124">Requirement</span></span> | <span data-ttu-id="edb54-125">Значение</span><span class="sxs-lookup"><span data-stu-id="edb54-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="edb54-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edb54-126">Minimum supported client</span></span><br/> | <span data-ttu-id="edb54-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="edb54-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edb54-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edb54-128">Minimum supported server</span></span><br/> | <span data-ttu-id="edb54-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="edb54-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="edb54-130">Header</span><span class="sxs-lookup"><span data-stu-id="edb54-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb54-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb54-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




