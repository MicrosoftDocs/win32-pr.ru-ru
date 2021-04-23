---
description: Возвращает список сохраненных файлов конфигурации резервных копий, которые можно восстановить.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Метод Листбаккупс класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140878"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="bc0c1-103">Метод Листбаккупс класса Control</span><span class="sxs-lookup"><span data-stu-id="bc0c1-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="bc0c1-104">Возвращает список сохраненных файлов конфигурации резервных копий, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="bc0c1-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc0c1-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="bc0c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc0c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0c1-107">*Оригиналтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c1-108">Метка времени установки текущей конфигурации (если она восстановлена из резервной копии, будет содержать исходную метку времени).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="bc0c1-109">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="bc0c1-110">*Оригиналтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c1-111">Метка времени установки текущей конфигурации (если она восстановлена из резервной копии, будет содержать исходную метку времени).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="bc0c1-112">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="bc0c1-113">*Файлы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c1-114">Список доступных файлов резервных копий в порядке от самых новых к старым.</span><span class="sxs-lookup"><span data-stu-id="bc0c1-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="bc0c1-115">*Филестиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c1-116">Для каждого файла резервной копии — метка времени, когда была задана ее конфигурация.</span><span class="sxs-lookup"><span data-stu-id="bc0c1-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="bc0c1-117">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="bc0c1-118">*Филестиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c1-119">Для каждого файла резервной копии — метка времени, когда была задана ее конфигурация.</span><span class="sxs-lookup"><span data-stu-id="bc0c1-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="bc0c1-120">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="bc0c1-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0c1-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc0c1-121">Return value</span></span>

<span data-ttu-id="bc0c1-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc0c1-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0c1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="bc0c1-123">Requirements</span></span>



| <span data-ttu-id="bc0c1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="bc0c1-124">Requirement</span></span> | <span data-ttu-id="bc0c1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="bc0c1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0c1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc0c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0c1-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bc0c1-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bc0c1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc0c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0c1-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bc0c1-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="bc0c1-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bc0c1-130">Namespace</span></span><br/>                | <span data-ttu-id="bc0c1-131">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="bc0c1-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="bc0c1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bc0c1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc0c1-133"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc0c1-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc0c1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc0c1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc0c1-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc0c1-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bc0c1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc0c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0c1-137">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="bc0c1-137">**Control**</span></span>](control.md)
</dt> </dl>

 

