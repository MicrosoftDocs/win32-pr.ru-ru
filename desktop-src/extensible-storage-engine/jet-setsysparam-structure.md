---
description: 'Дополнительные сведения: структура JET_SETSYSPARAM'
title: Структура JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342992"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="73343-103">Структура JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="73343-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="73343-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="73343-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="73343-105">Структура JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="73343-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="73343-106">Массив структур **JET_SETSYSPARAM** указывает конкретный набор глобальных системных параметров, которые задаются в качестве аргумента при использовании функции [жетенаблемултиинстанце](./jetenablemultiinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="73343-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="73343-107">**Windows XP:** Эта структура появилась в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73343-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="73343-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="73343-108">Members</span></span>

<span data-ttu-id="73343-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="73343-109">**paramid**</span></span>

<span data-ttu-id="73343-110">Идентификатор системного параметра, который будет установлен.</span><span class="sxs-lookup"><span data-stu-id="73343-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="73343-111">Полный список системных параметров и их свойств см. в разделе [расширяемые системные параметры](./extensible-storage-engine-system-parameters.md) подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="73343-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="73343-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="73343-112">**lParam**</span></span>

<span data-ttu-id="73343-113">Необязательное значение, устанавливаемое для выбранного системного параметра, если этот системный параметр имеет целочисленный тип.</span><span class="sxs-lookup"><span data-stu-id="73343-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="73343-114">**SZ**</span><span class="sxs-lookup"><span data-stu-id="73343-114">**sz**</span></span>

<span data-ttu-id="73343-115">Необязательное значение, устанавливаемое для выбранного системного параметра, если этот системный параметр имеет строковый тип.</span><span class="sxs-lookup"><span data-stu-id="73343-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="73343-116">**Err**</span><span class="sxs-lookup"><span data-stu-id="73343-116">**err**</span></span>

<span data-ttu-id="73343-117">Ошибка, полученная в результате вызова метода [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с указанными ранее параметрами.</span><span class="sxs-lookup"><span data-stu-id="73343-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="73343-118">Требования</span><span class="sxs-lookup"><span data-stu-id="73343-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73343-119"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="73343-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73343-120">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="73343-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73343-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="73343-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73343-122">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="73343-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73343-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="73343-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73343-124">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="73343-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73343-125"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="73343-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="73343-126">Реализуется как <strong>JET_ SETSYSPARAM_W</strong> (Юникод) и <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="73343-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="73343-127">См. также:</span><span class="sxs-lookup"><span data-stu-id="73343-127">See Also</span></span>

[<span data-ttu-id="73343-128">Параметры расширяемой системы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="73343-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="73343-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="73343-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="73343-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="73343-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="73343-131">жетенаблемултиинстанце</span><span class="sxs-lookup"><span data-stu-id="73343-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="73343-132">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="73343-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
