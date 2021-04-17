---
description: Функция Регопенблобкэй извлекает большой двоичный объект, хранящийся в указанном разделе реестра.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Функция Регопенблобкэй (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674419"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="1a78e-103">Функция Регопенблобкэй</span><span class="sxs-lookup"><span data-stu-id="1a78e-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="1a78e-104">Функция **регопенблобкэй** извлекает большой двоичный объект, хранящийся в указанном разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="1a78e-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a78e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a78e-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1a78e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a78e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a78e-107">*hKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a78e-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78e-108">Обработайте с ключом реестра, содержащим большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="1a78e-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1a78e-109">*сзблобнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a78e-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78e-110">Имя, идентифицирующее данный большой двоичный объект в реестре.</span><span class="sxs-lookup"><span data-stu-id="1a78e-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="1a78e-111">*фблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a78e-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78e-112">Указатель на возвращаемый большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="1a78e-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a78e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a78e-113">Return value</span></span>

<span data-ttu-id="1a78e-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1a78e-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1a78e-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1a78e-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a78e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1a78e-116">Requirements</span></span>



| <span data-ttu-id="1a78e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1a78e-117">Requirement</span></span> | <span data-ttu-id="1a78e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1a78e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a78e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a78e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a78e-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a78e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a78e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a78e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a78e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a78e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a78e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1a78e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a78e-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a78e-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1a78e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a78e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a78e-126"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a78e-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a78e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1a78e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a78e-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a78e-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a78e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a78e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a78e-130">регкреатеблобкэй</span><span class="sxs-lookup"><span data-stu-id="1a78e-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




