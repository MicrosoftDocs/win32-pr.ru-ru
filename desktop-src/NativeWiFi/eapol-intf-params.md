---
description: Содержит параметры конфигурации EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Структура EAPOL_INTF_PARAMS (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663569"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="76498-103">\_ \_ Структура params EAPOL intf</span><span class="sxs-lookup"><span data-stu-id="76498-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="76498-104">\[**EAPOL \_ \_Параметры intf** больше не поддерживаются в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="76498-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="76498-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="76498-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="76498-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="76498-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="76498-107">Содержит параметры конфигурации EAPOL.</span><span class="sxs-lookup"><span data-stu-id="76498-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="76498-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76498-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="76498-109">Члены</span><span class="sxs-lookup"><span data-stu-id="76498-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="76498-110">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="76498-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="76498-111">Версия вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="76498-111">Version of the caller.</span></span> <span data-ttu-id="76498-112">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="76498-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="76498-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="76498-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="76498-114">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="76498-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="76498-115">**двеапфлагс**</span><span class="sxs-lookup"><span data-stu-id="76498-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76498-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="76498-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="76498-117">**двеаптипе**</span><span class="sxs-lookup"><span data-stu-id="76498-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="76498-118">Используемый тип расширения EAP.</span><span class="sxs-lookup"><span data-stu-id="76498-118">The EAP extension type to be used.</span></span> <span data-ttu-id="76498-119">Задайте значение 0x00000013 для EAP-TLS и 0x00000026 для PEAP.</span><span class="sxs-lookup"><span data-stu-id="76498-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="76498-120">**двсизеофссид**</span><span class="sxs-lookup"><span data-stu-id="76498-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="76498-121">Размер идентификатора сети.</span><span class="sxs-lookup"><span data-stu-id="76498-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="76498-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="76498-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="76498-123">Идентификатор сети.</span><span class="sxs-lookup"><span data-stu-id="76498-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76498-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76498-124">Remarks</span></span>

<span data-ttu-id="76498-125">Файл заголовка взксапи. h недоступен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="76498-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="76498-126">Требования</span><span class="sxs-lookup"><span data-stu-id="76498-126">Requirements</span></span>



| <span data-ttu-id="76498-127">Требование</span><span class="sxs-lookup"><span data-stu-id="76498-127">Requirement</span></span> | <span data-ttu-id="76498-128">Значение</span><span class="sxs-lookup"><span data-stu-id="76498-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76498-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76498-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76498-130">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="76498-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76498-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76498-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76498-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76498-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76498-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="76498-133">End of client support</span></span><br/>    | <span data-ttu-id="76498-134">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="76498-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="76498-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="76498-135">End of server support</span></span><br/>    | <span data-ttu-id="76498-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76498-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="76498-137">Header</span><span class="sxs-lookup"><span data-stu-id="76498-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="76498-138"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="76498-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




