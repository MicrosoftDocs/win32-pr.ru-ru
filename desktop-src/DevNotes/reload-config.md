---
description: Перезагружает конфигурацию редактора IME из реестра HKCU в японском РЕДАКТОРЕ.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: Функция reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669285"
---
# <a name="reload_config-function"></a><span data-ttu-id="470e1-103">перезагрузка \_ функции конфигурации</span><span class="sxs-lookup"><span data-stu-id="470e1-103">reload\_config function</span></span>

<span data-ttu-id="470e1-104">Перезагружает конфигурацию редактора IME из реестра HKCU в японском РЕДАКТОРЕ.</span><span class="sxs-lookup"><span data-stu-id="470e1-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="470e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="470e1-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="470e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="470e1-106">Parameters</span></span>

<span data-ttu-id="470e1-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="470e1-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="470e1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="470e1-108">Return value</span></span>

<span data-ttu-id="470e1-109">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="470e1-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="470e1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="470e1-110">Remarks</span></span>

<span data-ttu-id="470e1-111">Если в HKCU не указано значение реестра, функция **перезагрузки \_ конфигурации** записывает исходные данные в реестр.</span><span class="sxs-lookup"><span data-stu-id="470e1-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="470e1-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="470e1-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="470e1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="470e1-113">Requirements</span></span>



| <span data-ttu-id="470e1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="470e1-114">Requirement</span></span> | <span data-ttu-id="470e1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="470e1-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470e1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="470e1-116">DLL</span></span><br/> | <dl> <span data-ttu-id="470e1-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="470e1-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
