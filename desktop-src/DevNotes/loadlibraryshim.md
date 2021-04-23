---
description: Загружает указанную версию библиотеки DLL платформа .NET Framework библиотеки.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Функция Лоадлибраришим
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665155"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="31290-103">Функция Лоадлибраришим</span><span class="sxs-lookup"><span data-stu-id="31290-103">LoadLibraryShim function</span></span>

<span data-ttu-id="31290-104">Загружает указанную версию библиотеки DLL платформа .NET Framework библиотеки.</span><span class="sxs-lookup"><span data-stu-id="31290-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="31290-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31290-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="31290-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31290-107">*сздллнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31290-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31290-108">Имя библиотеки DLL, загружаемой из платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="31290-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="31290-109">*сзверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31290-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31290-110">Версия загружаемой библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="31290-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="31290-111">Если *сзверсион* имеет **значение NULL**, загружается последняя версия указанной библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="31290-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="31290-112">*пвресервед*</span><span class="sxs-lookup"><span data-stu-id="31290-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="31290-113">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="31290-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="31290-114">*фмоддлл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31290-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31290-115">Обработчик для модуля.</span><span class="sxs-lookup"><span data-stu-id="31290-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31290-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31290-116">Return value</span></span>

<span data-ttu-id="31290-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="31290-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31290-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31290-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31290-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31290-119">Remarks</span></span>

<span data-ttu-id="31290-120">Эта функция используется для загрузки библиотек DLL библиотеки, включенных в распространяемый пакет платформа .NET Framework, а не для создаваемых пользователем библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="31290-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="31290-121">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="31290-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="31290-122">Требования</span><span class="sxs-lookup"><span data-stu-id="31290-122">Requirements</span></span>



| <span data-ttu-id="31290-123">Требование</span><span class="sxs-lookup"><span data-stu-id="31290-123">Requirement</span></span> | <span data-ttu-id="31290-124">Значение</span><span class="sxs-lookup"><span data-stu-id="31290-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31290-125">DLL</span><span class="sxs-lookup"><span data-stu-id="31290-125">DLL</span></span><br/> | <dl> <span data-ttu-id="31290-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31290-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
