---
description: Инициализирует таблицу строк.
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
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665252"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="e7f59-103">Функция Псетупстрингтаблеинитиализикс</span><span class="sxs-lookup"><span data-stu-id="e7f59-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="e7f59-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="e7f59-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="e7f59-105">Инициализирует таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="e7f59-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f59-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7f59-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="e7f59-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7f59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f59-108">*Екстрадатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7f59-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f59-109">Размер дополнительного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="e7f59-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="e7f59-110">*Зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7f59-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f59-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e7f59-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7f59-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7f59-112">Remarks</span></span>

<span data-ttu-id="e7f59-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e7f59-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f59-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e7f59-114">Requirements</span></span>



| <span data-ttu-id="e7f59-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e7f59-115">Requirement</span></span> | <span data-ttu-id="e7f59-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e7f59-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f59-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e7f59-117">DLL</span></span><br/> | <dl> <span data-ttu-id="e7f59-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7f59-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
