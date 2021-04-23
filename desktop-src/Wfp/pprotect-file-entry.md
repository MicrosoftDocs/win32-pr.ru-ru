---
description: Структура, используемая функцией Сфкжетфилес.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Структура PPROTECT_FILE_ENTRY (Сфкфилес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702301"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="60c58-103">\_ \_ Структура записи файла ппротект</span><span class="sxs-lookup"><span data-stu-id="60c58-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="60c58-104">\[Эта структура доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="60c58-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60c58-105">Поддержка этой структуры была удалена в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="60c58-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="60c58-106">Вместо этого используйте поддерживаемые функции, перечисленные в [функциях WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="60c58-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="60c58-107">Структура, используемая функцией [**сфкжетфилес**](sfcgetfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="60c58-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c58-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60c58-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="60c58-109">Члены</span><span class="sxs-lookup"><span data-stu-id="60c58-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="60c58-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="60c58-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="60c58-111">Указатель на строковое значение, содержащее имя файла исходного файла.</span><span class="sxs-lookup"><span data-stu-id="60c58-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="60c58-112">Это значение будет **равно NULL** , если файл не переименовывается при установке.</span><span class="sxs-lookup"><span data-stu-id="60c58-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="60c58-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="60c58-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="60c58-114">Указатель на строковое значение, содержащее имя файла назначения плюс полный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="60c58-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="60c58-115">**инфнаме**</span><span class="sxs-lookup"><span data-stu-id="60c58-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="60c58-116">Указатель на строковое значение, содержащее имя файла INF, который предоставляет сведения о макете.</span><span class="sxs-lookup"><span data-stu-id="60c58-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="60c58-117">При использовании макета по умолчанию этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="60c58-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60c58-118">Требования</span><span class="sxs-lookup"><span data-stu-id="60c58-118">Requirements</span></span>



| <span data-ttu-id="60c58-119">Требование</span><span class="sxs-lookup"><span data-stu-id="60c58-119">Requirement</span></span> | <span data-ttu-id="60c58-120">Значение</span><span class="sxs-lookup"><span data-stu-id="60c58-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60c58-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60c58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60c58-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="60c58-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="60c58-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60c58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60c58-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60c58-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60c58-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="60c58-125">End of client support</span></span><br/>    | <span data-ttu-id="60c58-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60c58-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="60c58-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="60c58-127">End of server support</span></span><br/>    | <span data-ttu-id="60c58-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60c58-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="60c58-129">Header</span><span class="sxs-lookup"><span data-stu-id="60c58-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c58-130"><dt>Сфкфилес. h</dt></span><span class="sxs-lookup"><span data-stu-id="60c58-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c58-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60c58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c58-132">**сфкжетфилес**</span><span class="sxs-lookup"><span data-stu-id="60c58-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




