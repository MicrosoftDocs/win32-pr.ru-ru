---
description: 'Дополнительные сведения: структура JET_LOGINFO'
title: Структура JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105694368"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="0e890-103">Структура JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="0e890-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="0e890-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0e890-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="0e890-105">Структура JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="0e890-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="0e890-106">Структура **JET_LOGINFO** возвращает структурированную информацию о наборе файлов журналов транзакций, которые должны быть частью набора файлов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="0e890-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="0e890-107">Структура **JET_LOGINFO** — это минимальный набор сведений, необходимых для представления диапазона журналов, получаемых с помощью [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) или указанных для жесткого восстановления с помощью [JetExternalRestore2](./jetexternalrestore2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0e890-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="0e890-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="0e890-108">Members</span></span>

<span data-ttu-id="0e890-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="0e890-109">**cbSize**</span></span>

<span data-ttu-id="0e890-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="0e890-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="0e890-111">Этот член обеспечивает будущее расширение этой структуры, одновременно обеспечивая обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="0e890-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="0e890-112">Для него всегда должно быть задано значение sizeof (JET_LOGINFO).</span><span class="sxs-lookup"><span data-stu-id="0e890-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="0e890-113">**улженлов**</span><span class="sxs-lookup"><span data-stu-id="0e890-113">**ulGenLow**</span></span>

<span data-ttu-id="0e890-114">Самый низкий (или самый старый) номер файла журнала, который восстанавливается.</span><span class="sxs-lookup"><span data-stu-id="0e890-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="0e890-115">Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0e890-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="0e890-116">Это может измениться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="0e890-116">This might change in future versions.</span></span>

<span data-ttu-id="0e890-117">**улженхигх**</span><span class="sxs-lookup"><span data-stu-id="0e890-117">**ulGenHigh**</span></span>

<span data-ttu-id="0e890-118">Самый высокий (или самый последний) номер файла журнала, который восстанавливается.</span><span class="sxs-lookup"><span data-stu-id="0e890-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="0e890-119">Необходимо сохранить полную достоверность беззнакового типа Long, но в текущей версии подсистемы это число является шестнадцатеричным числом в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0e890-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="0e890-120">Это может измениться в будущих версиях.</span><span class="sxs-lookup"><span data-stu-id="0e890-120">This might change in future versions.</span></span>

<span data-ttu-id="0e890-121">**сзбасенаме**</span><span class="sxs-lookup"><span data-stu-id="0e890-121">**szBaseName**</span></span>

<span data-ttu-id="0e890-122">Префикс, используемый для именования файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="0e890-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="0e890-123">Значение, возвращаемое в этом элементе, всегда равно значению параметра [JET_paramBaseName](./transaction-log-parameters.md) для экземпляра, который создал эти сведения.</span><span class="sxs-lookup"><span data-stu-id="0e890-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e890-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e890-124">Remarks</span></span>

<span data-ttu-id="0e890-125">Имена файлов журналов транзакций задаются в соответствии с базовым именем экземпляра и номером поколения файла журнала.</span><span class="sxs-lookup"><span data-stu-id="0e890-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="0e890-126">Имя имеет формат БББКСКСКСКСКС. Журналь.</span><span class="sxs-lookup"><span data-stu-id="0e890-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="0e890-127">BBB соответствует базовому имени файла журнала и всегда имеет три символа.</span><span class="sxs-lookup"><span data-stu-id="0e890-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="0e890-128">XXXXX соответствует номеру поколения файла журнала в шестнадцатеричном формате без дополнения и всегда имеет длину пять символов.</span><span class="sxs-lookup"><span data-stu-id="0e890-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="0e890-129">LOG — это расширение файла, которое всегда передается в файлы журнала транзакций ядром.</span><span class="sxs-lookup"><span data-stu-id="0e890-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="0e890-130">Использование этой структурированной информации не рекомендуется, так как оно заставляет приложение иметь глубокую информацию о схеме именования для файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="0e890-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="0e890-131">Если схема именования когда-либо изменится в будущем, это приложение перестанет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="0e890-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="0e890-132">Это представить, что формат журнала изменится на включение 8 шестнадцатеричных цифр в будущем.</span><span class="sxs-lookup"><span data-stu-id="0e890-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="0e890-133">Приложения должны использовать явный список имен файлов, возвращаемых функцией [жетжетлогинфо](./jetgetloginfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0e890-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="0e890-134">Требования</span><span class="sxs-lookup"><span data-stu-id="0e890-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e890-135"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0e890-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0e890-136">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e890-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e890-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0e890-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0e890-138">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e890-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e890-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0e890-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0e890-140">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0e890-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e890-141"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="0e890-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0e890-142">Реализуется как <strong>JET_LOGINFO_W</strong> (Юникод) и <strong>JET_LOGINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0e890-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0e890-143">См. также:</span><span class="sxs-lookup"><span data-stu-id="0e890-143">See Also</span></span>

[<span data-ttu-id="0e890-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="0e890-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="0e890-145">жетжетлогинфо</span><span class="sxs-lookup"><span data-stu-id="0e890-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="0e890-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="0e890-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="0e890-147">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="0e890-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
