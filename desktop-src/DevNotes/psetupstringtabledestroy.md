---
description: Удаляет таблицу строк.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: Функция Псетупстрингтабледестрой
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665257"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="e9205-103">Функция Псетупстрингтабледестрой</span><span class="sxs-lookup"><span data-stu-id="e9205-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="e9205-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="e9205-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="e9205-105">Удаляет таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="e9205-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9205-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9205-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="e9205-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9205-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9205-108">*STRINGTABLE* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9205-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9205-109">Указатель на таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="e9205-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9205-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9205-110">Return value</span></span>

<span data-ttu-id="e9205-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e9205-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9205-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9205-112">Remarks</span></span>

<span data-ttu-id="e9205-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e9205-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9205-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e9205-114">Requirements</span></span>



| <span data-ttu-id="e9205-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e9205-115">Requirement</span></span> | <span data-ttu-id="e9205-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e9205-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9205-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e9205-117">DLL</span></span><br/> | <dl> <span data-ttu-id="e9205-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9205-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
