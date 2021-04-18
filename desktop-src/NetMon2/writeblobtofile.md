---
description: Функция Вритеблобтофиле записывает большой двоичный объект в файл.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Функция Вритеблобтофиле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663968"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="6f0d5-103">Функция Вритеблобтофиле</span><span class="sxs-lookup"><span data-stu-id="6f0d5-103">WriteBlobToFile function</span></span>

<span data-ttu-id="6f0d5-104">Функция **вритеблобтофиле** ЗАПИСЫВАЕТ большой двоичный объект в файл.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f0d5-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="6f0d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f0d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0d5-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f0d5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0d5-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6f0d5-109">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f0d5-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0d5-110">Указатель на имя файла, в котором сохранен большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0d5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f0d5-111">Return value</span></span>

<span data-ttu-id="6f0d5-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6f0d5-113">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6f0d5-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f0d5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6f0d5-114">Requirements</span></span>



| <span data-ttu-id="6f0d5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6f0d5-115">Requirement</span></span> | <span data-ttu-id="6f0d5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6f0d5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0d5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f0d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f0d5-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f0d5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f0d5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f0d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f0d5-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f0d5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f0d5-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6f0d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f0d5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6f0d5-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f0d5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f0d5-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f0d5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6f0d5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f0d5-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d5-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




