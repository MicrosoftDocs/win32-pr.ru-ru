---
description: Инициализирует общий ресурс IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Функция Финитимешаре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657615"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="ff3f0-103">Функция Финитимешаре</span><span class="sxs-lookup"><span data-stu-id="ff3f0-103">FInitIMEShare function</span></span>

<span data-ttu-id="ff3f0-104">Инициализирует общий ресурс IME.</span><span class="sxs-lookup"><span data-stu-id="ff3f0-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff3f0-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="ff3f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff3f0-106">Parameters</span></span>

<span data-ttu-id="ff3f0-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ff3f0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff3f0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff3f0-108">Return value</span></span>

<span data-ttu-id="ff3f0-109">Функция возвращает **значение true** при успешном выполнении или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ff3f0-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff3f0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff3f0-110">Remarks</span></span>

<span data-ttu-id="ff3f0-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ff3f0-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="ff3f0-112">Эта функция должна вызываться до вызова любых других функций общего доступа IME.</span><span class="sxs-lookup"><span data-stu-id="ff3f0-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff3f0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ff3f0-113">Requirements</span></span>



| <span data-ttu-id="ff3f0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ff3f0-114">Requirement</span></span> | <span data-ttu-id="ff3f0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ff3f0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3f0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ff3f0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ff3f0-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff3f0-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff3f0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff3f0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3f0-119">**ендимешаре**</span><span class="sxs-lookup"><span data-stu-id="ff3f0-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
