---
description: Закрывает диспетчер OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Функция Октерминате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648083"
---
# <a name="octerminate-function"></a><span data-ttu-id="2dc0d-103">Функция Октерминате</span><span class="sxs-lookup"><span data-stu-id="2dc0d-103">OcTerminate function</span></span>

<span data-ttu-id="2dc0d-104">Закрывает диспетчер OC.</span><span class="sxs-lookup"><span data-stu-id="2dc0d-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dc0d-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="2dc0d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dc0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc0d-107">*Окманажерконтекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2dc0d-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc0d-108">На входе содержит указатель контекста диспетчера OC, возвращенный [**оЦинитиализе**](ocinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="2dc0d-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="2dc0d-109">На выходе получает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2dc0d-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc0d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dc0d-110">Return value</span></span>

<span data-ttu-id="2dc0d-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2dc0d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc0d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dc0d-112">Remarks</span></span>

<span data-ttu-id="2dc0d-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2dc0d-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc0d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc0d-114">Requirements</span></span>



| <span data-ttu-id="2dc0d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc0d-115">Requirement</span></span> | <span data-ttu-id="2dc0d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc0d-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc0d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2dc0d-117">DLL</span></span><br/> | <dl> <span data-ttu-id="2dc0d-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc0d-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc0d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dc0d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc0d-120">**оЦинитиализе**</span><span class="sxs-lookup"><span data-stu-id="2dc0d-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
