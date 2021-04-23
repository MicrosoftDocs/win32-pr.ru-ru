---
description: Завершает наблюдение за неактивностью.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Функция Ендидледетектион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648771"
---
# <a name="endidledetection-function"></a><span data-ttu-id="dffee-103">Функция Ендидледетектион</span><span class="sxs-lookup"><span data-stu-id="dffee-103">EndIdleDetection function</span></span>

<span data-ttu-id="dffee-104">\[Эта функция не поддерживается и может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="dffee-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="dffee-105">Вместо этого используйте функцию **жетластинпутинфо** .\]</span><span class="sxs-lookup"><span data-stu-id="dffee-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="dffee-106">Завершает наблюдение за неактивностью.</span><span class="sxs-lookup"><span data-stu-id="dffee-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dffee-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="dffee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dffee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffee-109">*двресервед*</span><span class="sxs-lookup"><span data-stu-id="dffee-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="dffee-110">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="dffee-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffee-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dffee-111">Return value</span></span>

<span data-ttu-id="dffee-112">Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dffee-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dffee-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dffee-113">Remarks</span></span>

<span data-ttu-id="dffee-114">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="dffee-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="dffee-115">Эта функция не экспортируется по имени; Укажите порядковый номер 4 при вызове **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="dffee-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffee-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dffee-116">Requirements</span></span>



| <span data-ttu-id="dffee-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dffee-117">Requirement</span></span> | <span data-ttu-id="dffee-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dffee-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dffee-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dffee-119">DLL</span></span><br/> | <dl> <span data-ttu-id="dffee-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dffee-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffee-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dffee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffee-122">**жетластинпутинфо**</span><span class="sxs-lookup"><span data-stu-id="dffee-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
