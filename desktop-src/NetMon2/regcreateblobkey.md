---
description: Функция Регкреатеблобкэй сохраняет большой двоичный объект в заданном разделе реестра.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Функция Регкреатеблобкэй (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674420"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="63af7-103">Функция Регкреатеблобкэй</span><span class="sxs-lookup"><span data-stu-id="63af7-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="63af7-104">Функция **регкреатеблобкэй** сохраняет большой двоичный объект в заданном разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="63af7-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="63af7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63af7-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="63af7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63af7-107">*hKey* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63af7-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63af7-108">Обработайте с разделом реестра, в котором будет храниться большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="63af7-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="63af7-109">*сзблобнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63af7-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63af7-110">Имя (определяется приложением), представляющее большой двоичный объект в реестре.</span><span class="sxs-lookup"><span data-stu-id="63af7-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="63af7-111">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63af7-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63af7-112">Обработчик сохраняемого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="63af7-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63af7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63af7-113">Return value</span></span>

<span data-ttu-id="63af7-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="63af7-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="63af7-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="63af7-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="63af7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="63af7-116">Requirements</span></span>



| <span data-ttu-id="63af7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="63af7-117">Requirement</span></span> | <span data-ttu-id="63af7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="63af7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63af7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63af7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63af7-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63af7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63af7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63af7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63af7-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63af7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63af7-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63af7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63af7-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63af7-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="63af7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63af7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="63af7-126"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63af7-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="63af7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="63af7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63af7-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63af7-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63af7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63af7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63af7-130">регопенблобкэй</span><span class="sxs-lookup"><span data-stu-id="63af7-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




