---
description: Содержит таблицу основных сведений для всех интерфейсов беспроводной локальной сети, управляемых службой настройки беспроводной связи.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Структура INTFS_KEY_TABLE (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662488"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="95550-103">\_ \_ Структура таблицы ключей интфс</span><span class="sxs-lookup"><span data-stu-id="95550-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="95550-104">\[**Интфс \_ \_Таблица ключей** больше не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="95550-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="95550-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="95550-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="95550-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="95550-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="95550-107">Структура **\_ \_ таблицы ключей интфс** содержит таблицу основных сведений для всех интерфейсов беспроводной локальной сети, управляемых службой настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="95550-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="95550-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95550-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="95550-109">Члены</span><span class="sxs-lookup"><span data-stu-id="95550-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="95550-110">**двнуминтфс**</span><span class="sxs-lookup"><span data-stu-id="95550-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="95550-111">Общее число интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="95550-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="95550-112">**пинтфс**</span><span class="sxs-lookup"><span data-stu-id="95550-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="95550-113">Указатель на структуру [**\_ \_ записи ключа intf**](intf-key-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="95550-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95550-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95550-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95550-115">Файл заголовка *взксапи. h* недоступен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="95550-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95550-116">Требования</span><span class="sxs-lookup"><span data-stu-id="95550-116">Requirements</span></span>



| <span data-ttu-id="95550-117">Требование</span><span class="sxs-lookup"><span data-stu-id="95550-117">Requirement</span></span> | <span data-ttu-id="95550-118">Значение</span><span class="sxs-lookup"><span data-stu-id="95550-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95550-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95550-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95550-120">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="95550-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95550-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95550-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95550-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95550-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95550-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="95550-123">End of client support</span></span><br/>    | <span data-ttu-id="95550-124">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="95550-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="95550-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="95550-125">End of server support</span></span><br/>    | <span data-ttu-id="95550-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95550-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="95550-127">Header</span><span class="sxs-lookup"><span data-stu-id="95550-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95550-128"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="95550-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




