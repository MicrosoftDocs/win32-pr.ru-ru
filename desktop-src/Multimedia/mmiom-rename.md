---
title: Сообщение MMIOM_RENAME (Ммсистем. h)
description: '\_Сообщение о переименовании ммиом отправляется в процедуру ввода-вывода функцией ммиоренаме, чтобы запросить переименование указанного файла.'
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492348"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="90db3-104">ММИОМ \_ Переименование сообщения</span><span class="sxs-lookup"><span data-stu-id="90db3-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="90db3-105">Сообщение **о \_ переименовании ммиом** отправляется в процедуру ввода-вывода функцией [**ммиоренаме**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) , чтобы запросить переименование указанного файла.</span><span class="sxs-lookup"><span data-stu-id="90db3-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="90db3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90db3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90db3-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*лпсзолдфиленаме*</span><span class="sxs-lookup"><span data-stu-id="90db3-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="90db3-108">Указатель на строку, содержащую имя файла для переименования.</span><span class="sxs-lookup"><span data-stu-id="90db3-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="90db3-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*лпсзневфиленаме*</span><span class="sxs-lookup"><span data-stu-id="90db3-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="90db3-110">Указатель на строку, содержащую новое имя файла.</span><span class="sxs-lookup"><span data-stu-id="90db3-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90db3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90db3-111">Return Value</span></span>

<span data-ttu-id="90db3-112">Если файл успешно переименован, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90db3-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="90db3-113">Если указанный файл не найден, возвращается значение ММИОЕРР \_ FILENOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="90db3-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="90db3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="90db3-114">Requirements</span></span>



| <span data-ttu-id="90db3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="90db3-115">Requirement</span></span> | <span data-ttu-id="90db3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="90db3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90db3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90db3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="90db3-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90db3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="90db3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90db3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="90db3-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90db3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90db3-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="90db3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="90db3-122"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90db3-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

