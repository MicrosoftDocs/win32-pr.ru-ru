---
title: Класс MSAD_ReplCursor
description: Предоставляет сведения о состоянии входящей репликации о всех репликах заданного контекста именования (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplCursor Active Directory
- Active Directory класса MSAD_ReplCursor, описание
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490737"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="97e3e-105">\_Класс МСАД реплкурсор</span><span class="sxs-lookup"><span data-stu-id="97e3e-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="97e3e-106">Предоставляет сведения о состоянии входящей репликации о всех репликах заданного контекста именования (NC).</span><span class="sxs-lookup"><span data-stu-id="97e3e-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="97e3e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97e3e-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="97e3e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="97e3e-108">Members</span></span>

<span data-ttu-id="97e3e-109">Класс **МСАД \_ реплкурсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97e3e-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="97e3e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="97e3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97e3e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="97e3e-111">Properties</span></span>

<span data-ttu-id="97e3e-112">Класс **МСАД \_ реплкурсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97e3e-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97e3e-113">**намингконтекстдн**</span><span class="sxs-lookup"><span data-stu-id="97e3e-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e3e-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97e3e-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97e3e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-116">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97e3e-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="97e3e-117">Возвращает путь X. 500 для контекста именования (NC), содержащего этот курсор.</span><span class="sxs-lookup"><span data-stu-id="97e3e-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="97e3e-118">**саурцедсадн**</span><span class="sxs-lookup"><span data-stu-id="97e3e-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e3e-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97e3e-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97e3e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97e3e-121">Возвращает путь X. 500 к системному агенту каталога (DSA), который представляет исходный контроллер домена (DC).</span><span class="sxs-lookup"><span data-stu-id="97e3e-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="97e3e-122">**саурцедсаинвокатионид**</span><span class="sxs-lookup"><span data-stu-id="97e3e-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e3e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97e3e-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97e3e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97e3e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="97e3e-126">Возвращает идентификатор вызова исходного сервера, которому соответствует **уснаттрибутефилтер** .</span><span class="sxs-lookup"><span data-stu-id="97e3e-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="97e3e-127">**тимеофластсукцессфулсинк**</span><span class="sxs-lookup"><span data-stu-id="97e3e-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e3e-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97e3e-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97e3e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97e3e-130">Возвращает метку времени последней успешной синхронизации репликации с исходным DSA.</span><span class="sxs-lookup"><span data-stu-id="97e3e-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="97e3e-131">Указывает время, в течение которого этот контроллер домена покажет изменения, внесенные в исходный DSA для этого сетевого контроллера.</span><span class="sxs-lookup"><span data-stu-id="97e3e-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="97e3e-132">**уснаттрибутефилтер**</span><span class="sxs-lookup"><span data-stu-id="97e3e-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e3e-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="97e3e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="97e3e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97e3e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97e3e-135">Возвращает максимальный порядковый номер обновления, по которому целевой сервер может указать, что он записал все изменения, порожденные данным сервером, по порядковым номерам обновления, меньшим или равным, этим порядковым номером обновления.</span><span class="sxs-lookup"><span data-stu-id="97e3e-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="97e3e-136">Это свойство используется для фильтрации изменений, которые сервер назначения уже применил к исходным серверам репликации.</span><span class="sxs-lookup"><span data-stu-id="97e3e-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97e3e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="97e3e-137">Requirements</span></span>



| <span data-ttu-id="97e3e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="97e3e-138">Requirement</span></span> | <span data-ttu-id="97e3e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="97e3e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97e3e-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97e3e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="97e3e-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97e3e-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="97e3e-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97e3e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="97e3e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97e3e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97e3e-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97e3e-144">Namespace</span></span><br/>                | <span data-ttu-id="97e3e-145">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="97e3e-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="97e3e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="97e3e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97e3e-147"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97e3e-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="97e3e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="97e3e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e3e-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97e3e-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e3e-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97e3e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e3e-151">**\_курсор REPL в DS \_**</span><span class="sxs-lookup"><span data-stu-id="97e3e-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

