---
description: Функция Реадблобфромфиле считывает большой двоичный объект в файле.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Функция Реадблобфромфиле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674422"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="741e5-103">Функция Реадблобфромфиле</span><span class="sxs-lookup"><span data-stu-id="741e5-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="741e5-104">Функция **реадблобфромфиле** считывает большой двоичный объект в файле.</span><span class="sxs-lookup"><span data-stu-id="741e5-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="741e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="741e5-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="741e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="741e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741e5-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="741e5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741e5-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="741e5-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="741e5-109">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="741e5-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741e5-110">Указатель на имя файла, содержащего большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="741e5-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741e5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="741e5-111">Return value</span></span>

<span data-ttu-id="741e5-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="741e5-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="741e5-113">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="741e5-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="741e5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="741e5-114">Requirements</span></span>



| <span data-ttu-id="741e5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="741e5-115">Requirement</span></span> | <span data-ttu-id="741e5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="741e5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="741e5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="741e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="741e5-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="741e5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="741e5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="741e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="741e5-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="741e5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="741e5-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="741e5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="741e5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="741e5-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="741e5-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="741e5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="741e5-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="741e5-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="741e5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="741e5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="741e5-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="741e5-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




