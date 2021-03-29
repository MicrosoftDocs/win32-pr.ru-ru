---
description: Декодирует и сохраняет строку.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Функция CchLszOfId2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657785"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="f37d9-103">Функция CchLszOfId2</span><span class="sxs-lookup"><span data-stu-id="f37d9-103">CchLszOfId2 function</span></span>

<span data-ttu-id="f37d9-104">Декодирует и сохраняет строку.</span><span class="sxs-lookup"><span data-stu-id="f37d9-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f37d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f37d9-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="f37d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f37d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f37d9-107">*id*</span><span class="sxs-lookup"><span data-stu-id="f37d9-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="f37d9-108">Идентификатор строки в файле ресурсов для декодирования и сохранения.</span><span class="sxs-lookup"><span data-stu-id="f37d9-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="f37d9-109">Допустимость строки не проверяется.</span><span class="sxs-lookup"><span data-stu-id="f37d9-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="f37d9-110">*лсз*</span><span class="sxs-lookup"><span data-stu-id="f37d9-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="f37d9-111">Указатель на буфер с длиной *кбмакс*.</span><span class="sxs-lookup"><span data-stu-id="f37d9-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="f37d9-112">Строки, длина которых превышает *кбмакс* , усекаются.</span><span class="sxs-lookup"><span data-stu-id="f37d9-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="f37d9-113">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="f37d9-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="f37d9-114">Максимальная длина строки, сохраняемой в параметре *лсз* .</span><span class="sxs-lookup"><span data-stu-id="f37d9-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f37d9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f37d9-115">Return value</span></span>

<span data-ttu-id="f37d9-116">Эта функция возвращает декодированную строку.</span><span class="sxs-lookup"><span data-stu-id="f37d9-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f37d9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f37d9-117">Remarks</span></span>

<span data-ttu-id="f37d9-118">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f37d9-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f37d9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f37d9-119">Requirements</span></span>



| <span data-ttu-id="f37d9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f37d9-120">Requirement</span></span> | <span data-ttu-id="f37d9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f37d9-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f37d9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f37d9-122">DLL</span></span><br/> | <dl> <span data-ttu-id="f37d9-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f37d9-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
