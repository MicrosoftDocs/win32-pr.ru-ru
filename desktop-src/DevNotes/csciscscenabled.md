---
description: Определяет, включена ли автономные файлы.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: Функция КсЦисксценаблед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657767"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="b45f2-103">Функция КсЦисксценаблед</span><span class="sxs-lookup"><span data-stu-id="b45f2-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="b45f2-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="b45f2-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="b45f2-105">Определяет, включена ли автономные файлы.</span><span class="sxs-lookup"><span data-stu-id="b45f2-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b45f2-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="b45f2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b45f2-107">Parameters</span></span>

<span data-ttu-id="b45f2-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="b45f2-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b45f2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b45f2-109">Return value</span></span>

<span data-ttu-id="b45f2-110">Эта функция возвращает **значение true** , если автономные файлы включена, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b45f2-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45f2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b45f2-111">Remarks</span></span>

<span data-ttu-id="b45f2-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b45f2-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45f2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b45f2-113">Requirements</span></span>



| <span data-ttu-id="b45f2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b45f2-114">Requirement</span></span> | <span data-ttu-id="b45f2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b45f2-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b45f2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b45f2-116">DLL</span></span><br/> | <dl> <span data-ttu-id="b45f2-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b45f2-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45f2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b45f2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45f2-119">**ксккуеридатабасестатус**</span><span class="sxs-lookup"><span data-stu-id="b45f2-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
