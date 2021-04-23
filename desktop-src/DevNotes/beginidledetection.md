---
description: Начинает мониторинг неактивности.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Функция Бегинидледетектион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668847"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="916b4-103">Функция Бегинидледетектион</span><span class="sxs-lookup"><span data-stu-id="916b4-103">BeginIdleDetection function</span></span>

<span data-ttu-id="916b4-104">\[Эта функция не поддерживается и может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="916b4-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="916b4-105">Вместо этого используйте функцию **жетластинпутинфо** .\]</span><span class="sxs-lookup"><span data-stu-id="916b4-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="916b4-106">Начинает мониторинг неактивности.</span><span class="sxs-lookup"><span data-stu-id="916b4-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="916b4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="916b4-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="916b4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="916b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="916b4-109">*пфнкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="916b4-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="916b4-110">Функция, которая вызывается при изменении состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="916b4-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="916b4-111">Этот обратный вызов определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="916b4-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="916b4-112">*двидлемин*</span><span class="sxs-lookup"><span data-stu-id="916b4-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="916b4-113">Число минут бездействия до вызова функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="916b4-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="916b4-114">*двресервед*</span><span class="sxs-lookup"><span data-stu-id="916b4-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="916b4-115">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="916b4-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="916b4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="916b4-116">Return value</span></span>

<span data-ttu-id="916b4-117">Возвращает 0, если функция выполнена. в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="916b4-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="916b4-118">Например, если *двресервед* имеет значение, отличное от 0, **возвращаются \_ недопустимые \_ данные** .</span><span class="sxs-lookup"><span data-stu-id="916b4-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="916b4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="916b4-119">Remarks</span></span>

<span data-ttu-id="916b4-120">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="916b4-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="916b4-121">Эта функция не экспортируется по имени; Укажите порядковый номер 3 при вызове **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="916b4-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="916b4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="916b4-122">Requirements</span></span>



| <span data-ttu-id="916b4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="916b4-123">Requirement</span></span> | <span data-ttu-id="916b4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="916b4-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="916b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="916b4-125">DLL</span></span><br/> | <dl> <span data-ttu-id="916b4-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="916b4-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916b4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="916b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916b4-128">**жетластинпутинфо**</span><span class="sxs-lookup"><span data-stu-id="916b4-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
