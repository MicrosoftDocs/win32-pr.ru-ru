---
description: Хранит основные сведения об интерфейсе беспроводной локальной сети, управляемом службой настройки беспроводной связи.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Структура INTF_KEY_ENTRY (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343895"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="20965-103">\_ \_ Структура ввода ключа intf</span><span class="sxs-lookup"><span data-stu-id="20965-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="20965-104">\[**Intf \_ \_Запись ключа** больше не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="20965-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="20965-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="20965-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="20965-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="20965-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="20965-107">В **структуре \_ \_ ввода ключа intf** хранятся основные сведения об интерфейсе беспроводной локальной сети, управляемом службой настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="20965-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="20965-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20965-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="20965-109">Члены</span><span class="sxs-lookup"><span data-stu-id="20965-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="20965-110">**всзгуид**</span><span class="sxs-lookup"><span data-stu-id="20965-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="20965-111">Указатель на идентификатор GUID интерфейса, представленный в виде строки в Юникоде в следующем формате: "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="20965-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20965-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20965-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20965-113">Файл заголовка *взксапи. h* недоступен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="20965-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20965-114">Требования</span><span class="sxs-lookup"><span data-stu-id="20965-114">Requirements</span></span>



| <span data-ttu-id="20965-115">Требование</span><span class="sxs-lookup"><span data-stu-id="20965-115">Requirement</span></span> | <span data-ttu-id="20965-116">Значение</span><span class="sxs-lookup"><span data-stu-id="20965-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20965-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20965-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20965-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="20965-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="20965-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20965-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20965-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20965-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="20965-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="20965-121">End of client support</span></span><br/>    | <span data-ttu-id="20965-122">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="20965-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="20965-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="20965-123">End of server support</span></span><br/>    | <span data-ttu-id="20965-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="20965-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="20965-125">Header</span><span class="sxs-lookup"><span data-stu-id="20965-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20965-126"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="20965-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20965-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20965-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20965-128">**\_Таблица ключей \_ интфс**</span><span class="sxs-lookup"><span data-stu-id="20965-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="20965-129">**взценуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="20965-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




