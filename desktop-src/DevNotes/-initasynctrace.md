---
description: Инициализирует трассировку.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Функция Инитасинктраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648028"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="da684-103">Функция Инитасинктраце</span><span class="sxs-lookup"><span data-stu-id="da684-103">InitAsyncTrace function</span></span>

<span data-ttu-id="da684-104">Инициализирует трассировку.</span><span class="sxs-lookup"><span data-stu-id="da684-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="da684-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da684-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="da684-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da684-106">Parameters</span></span>

<span data-ttu-id="da684-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="da684-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da684-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da684-108">Return value</span></span>

<span data-ttu-id="da684-109">Эта функция возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="da684-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da684-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da684-110">Remarks</span></span>

<span data-ttu-id="da684-111">Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.</span><span class="sxs-lookup"><span data-stu-id="da684-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="da684-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="da684-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="da684-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da684-113">Requirements</span></span>



| <span data-ttu-id="da684-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da684-114">Requirement</span></span> | <span data-ttu-id="da684-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da684-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da684-116">DLL</span><span class="sxs-lookup"><span data-stu-id="da684-116">DLL</span></span><br/> | <dl> <span data-ttu-id="da684-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da684-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
