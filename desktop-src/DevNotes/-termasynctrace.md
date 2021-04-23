---
description: Завершает трассировку.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: Функция Термасинктраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648985"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="33fa9-103">Функция Термасинктраце</span><span class="sxs-lookup"><span data-stu-id="33fa9-103">TermAsyncTrace function</span></span>

<span data-ttu-id="33fa9-104">Завершает трассировку.</span><span class="sxs-lookup"><span data-stu-id="33fa9-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fa9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33fa9-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="33fa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33fa9-106">Parameters</span></span>

<span data-ttu-id="33fa9-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="33fa9-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33fa9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33fa9-108">Return value</span></span>

<span data-ttu-id="33fa9-109">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="33fa9-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="33fa9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33fa9-110">Remarks</span></span>

<span data-ttu-id="33fa9-111">Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.</span><span class="sxs-lookup"><span data-stu-id="33fa9-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="33fa9-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="33fa9-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fa9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="33fa9-113">Requirements</span></span>



| <span data-ttu-id="33fa9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="33fa9-114">Requirement</span></span> | <span data-ttu-id="33fa9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="33fa9-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33fa9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="33fa9-116">DLL</span></span><br/> | <dl> <span data-ttu-id="33fa9-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fa9-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
