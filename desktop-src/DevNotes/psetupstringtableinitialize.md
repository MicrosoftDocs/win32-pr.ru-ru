---
description: Инициализирует таблицу строк.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: Функция Псетупстрингтаблеинитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665255"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="709c8-103">Функция Псетупстрингтаблеинитиализе</span><span class="sxs-lookup"><span data-stu-id="709c8-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="709c8-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="709c8-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="709c8-105">Инициализирует таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="709c8-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="709c8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="709c8-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="709c8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="709c8-107">Parameters</span></span>

<span data-ttu-id="709c8-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="709c8-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="709c8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="709c8-109">Remarks</span></span>

<span data-ttu-id="709c8-110">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="709c8-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="709c8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="709c8-111">Requirements</span></span>



| <span data-ttu-id="709c8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="709c8-112">Requirement</span></span> | <span data-ttu-id="709c8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="709c8-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="709c8-114">DLL</span><span class="sxs-lookup"><span data-stu-id="709c8-114">DLL</span></span><br/> | <dl> <span data-ttu-id="709c8-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709c8-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
