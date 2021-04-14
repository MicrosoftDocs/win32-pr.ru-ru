---
description: Освобождает загрузчики классов Java, которые могли использоваться при просмотре приложений.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Функция Нотифибровсершутдовн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668482"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="3deea-103">Функция Нотифибровсершутдовн</span><span class="sxs-lookup"><span data-stu-id="3deea-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="3deea-104">Освобождает загрузчики классов Java, которые могли использоваться при просмотре приложений.</span><span class="sxs-lookup"><span data-stu-id="3deea-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="3deea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3deea-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="3deea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3deea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3deea-107">*лпвресервед*</span><span class="sxs-lookup"><span data-stu-id="3deea-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="3deea-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3deea-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3deea-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3deea-109">Return value</span></span>

<span data-ttu-id="3deea-110">Если функция выполнена успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3deea-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="3deea-111">В противном случае возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="3deea-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3deea-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3deea-112">Remarks</span></span>

<span data-ttu-id="3deea-113">Когда число окон браузера достигает нуля в интегрированном веб-режиме, эта функция освобождает загрузчики классов Java.</span><span class="sxs-lookup"><span data-stu-id="3deea-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="3deea-114">Когда пользователь снова начинает просмотр приложений, виртуальная машина Java загрузит последние файлы классов.</span><span class="sxs-lookup"><span data-stu-id="3deea-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="3deea-115">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3deea-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3deea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3deea-116">Requirements</span></span>



| <span data-ttu-id="3deea-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3deea-117">Requirement</span></span> | <span data-ttu-id="3deea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3deea-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3deea-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3deea-119">DLL</span></span><br/> | <dl> <span data-ttu-id="3deea-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3deea-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
