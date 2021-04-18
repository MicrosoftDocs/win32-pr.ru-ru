---
description: Завершает общий ресурс IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Функция Ендимешаре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656887"
---
# <a name="endimeshare-function"></a><span data-ttu-id="4625d-103">Функция Ендимешаре</span><span class="sxs-lookup"><span data-stu-id="4625d-103">EndIMEShare function</span></span>

<span data-ttu-id="4625d-104">Завершает общий ресурс IME.</span><span class="sxs-lookup"><span data-stu-id="4625d-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="4625d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4625d-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="4625d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4625d-106">Parameters</span></span>

<span data-ttu-id="4625d-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4625d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4625d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4625d-108">Return value</span></span>

<span data-ttu-id="4625d-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4625d-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4625d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4625d-110">Remarks</span></span>

<span data-ttu-id="4625d-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4625d-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="4625d-112">Эта функция должна вызываться после вызова последней функции общего ресурса IME.</span><span class="sxs-lookup"><span data-stu-id="4625d-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="4625d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4625d-113">Requirements</span></span>



| <span data-ttu-id="4625d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4625d-114">Requirement</span></span> | <span data-ttu-id="4625d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4625d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4625d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4625d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4625d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4625d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4625d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4625d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4625d-119">**финитимешаре**</span><span class="sxs-lookup"><span data-stu-id="4625d-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
