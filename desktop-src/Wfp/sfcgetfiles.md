---
description: Список защищенных файлов.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Функция Сфкжетфилес (Сфкфилес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910595"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="501e2-103">Функция Сфкжетфилес</span><span class="sxs-lookup"><span data-stu-id="501e2-103">SfcGetFiles function</span></span>

<span data-ttu-id="501e2-104">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="501e2-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="501e2-105">Поддержка этой функции была удалена в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="501e2-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="501e2-106">Вместо этого используйте поддерживаемые функции, перечисленные в [функциях WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="501e2-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="501e2-107">Список защищенных файлов.</span><span class="sxs-lookup"><span data-stu-id="501e2-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="501e2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="501e2-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="501e2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="501e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="501e2-110">*Протфиледата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="501e2-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="501e2-111">Указатель на структуру [**\_ \_ записи файла ппротект**](pprotect-file-entry.md) , содержащую список защищенных файлов.</span><span class="sxs-lookup"><span data-stu-id="501e2-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="501e2-112">*Filecount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="501e2-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="501e2-113">Указатель на расположение, содержащее значение ULONG, которое является числом защищенных файлов.</span><span class="sxs-lookup"><span data-stu-id="501e2-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="501e2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="501e2-114">Return value</span></span>

<span data-ttu-id="501e2-115">Если функция завершается успешно, возвращается значение STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="501e2-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="501e2-116">Если функция завершается с ошибкой, возвращается соответствующий код ошибки NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="501e2-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="501e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="501e2-117">Requirements</span></span>



| <span data-ttu-id="501e2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="501e2-118">Requirement</span></span> | <span data-ttu-id="501e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="501e2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="501e2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="501e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="501e2-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="501e2-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="501e2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="501e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="501e2-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="501e2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="501e2-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="501e2-124">End of client support</span></span><br/>    | <span data-ttu-id="501e2-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="501e2-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="501e2-126">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="501e2-126">End of server support</span></span><br/>    | <span data-ttu-id="501e2-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="501e2-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="501e2-128">Header</span><span class="sxs-lookup"><span data-stu-id="501e2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="501e2-129"><dt>Сфкфилес. h</dt></span><span class="sxs-lookup"><span data-stu-id="501e2-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="501e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="501e2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501e2-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="501e2-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="501e2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="501e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501e2-133">**\_запись файла \_ ппротект**</span><span class="sxs-lookup"><span data-stu-id="501e2-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




