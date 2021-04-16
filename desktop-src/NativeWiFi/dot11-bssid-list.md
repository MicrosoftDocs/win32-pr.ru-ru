---
description: Содержит список идентификаторов "базовый набор служб (BSS)".
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Структура DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683668"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="8e792-103">\_ \_ Структура списка BSSID DOT11</span><span class="sxs-lookup"><span data-stu-id="8e792-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="8e792-104">Структура **\_ \_ списка BSSID для DOT11** содержит список основных идентификаторов набора служб (BSS).</span><span class="sxs-lookup"><span data-stu-id="8e792-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e792-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e792-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="8e792-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8e792-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e792-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="8e792-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="8e792-108">Структура [**\_ \_ заголовка объекта NDIS**](ndis-object-header.md) , содержащая сведения о типе, версии и размере структуры NDIS.</span><span class="sxs-lookup"><span data-stu-id="8e792-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="8e792-109">Для большинства **структур \_ \_ списка BSSID DOT11** установите для элемента **типа** значение **\_ \_ \_ по умолчанию тип объекта NDIS**, установите для элемента **Revision** значение **DOT11, \_ \_ \_ редакция \_ 1**, и задайте для элемента **size** значение **sizeof ( \_ список DOT11 BSSID \_ )**.</span><span class="sxs-lookup"><span data-stu-id="8e792-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="8e792-110">**унумофентриес**</span><span class="sxs-lookup"><span data-stu-id="8e792-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8e792-111">Число записей в этой структуре.</span><span class="sxs-lookup"><span data-stu-id="8e792-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="8e792-112">**утоталнумофентриес**</span><span class="sxs-lookup"><span data-stu-id="8e792-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8e792-113">Общее число поддерживаемых записей.</span><span class="sxs-lookup"><span data-stu-id="8e792-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e792-114">**бссидс**</span><span class="sxs-lookup"><span data-stu-id="8e792-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="8e792-115">Список идентификаторов BSS.</span><span class="sxs-lookup"><span data-stu-id="8e792-115">A list of BSS identifiers.</span></span> <span data-ttu-id="8e792-116">Идентификатор BSS хранится в виде типа [**\_ Mac- \_ адреса DOT11**](dot11-mac-address-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8e792-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e792-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8e792-117">Requirements</span></span>



| <span data-ttu-id="8e792-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8e792-118">Requirement</span></span> | <span data-ttu-id="8e792-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8e792-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e792-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e792-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e792-121">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e792-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e792-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e792-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e792-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e792-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8e792-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8e792-124">Redistributable</span></span><br/>          | <span data-ttu-id="8e792-125">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="8e792-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="8e792-126">Header</span><span class="sxs-lookup"><span data-stu-id="8e792-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e792-127"><dt>Windot11. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e792-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e792-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e792-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e792-129">**\_Параметры подключения \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="8e792-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




