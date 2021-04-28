---
description: Функция Псетупстрингтаблеинитиализикс — инициализирует таблицу строк.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Функция Псетупстрингтаблеинитиализикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096652"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="2d2d9-103">Функция Псетупстрингтаблеинитиализикс</span><span class="sxs-lookup"><span data-stu-id="2d2d9-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="2d2d9-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="2d2d9-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="2d2d9-105">Инициализирует таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d2d9-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="2d2d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d2d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d2d9-108">*Екстрадатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d2d9-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d2d9-109">Размер дополнительного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="2d2d9-110">*Зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d2d9-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d2d9-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d2d9-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="2d2d9-112">Remarks</span></span>

<span data-ttu-id="2d2d9-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2d2d9-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2d9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2d2d9-114">Requirements</span></span>



| <span data-ttu-id="2d2d9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2d2d9-115">Requirement</span></span> | <span data-ttu-id="2d2d9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2d2d9-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2d9-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2d9-117">DLL</span></span><br/> | <dl> <span data-ttu-id="2d2d9-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d2d9-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
