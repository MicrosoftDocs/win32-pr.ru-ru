---
description: Указывает версию CTL3D сегодня, которая выполняется в данный момент.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Функция Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648972"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="c44c8-103">Функция Ctl3dGetVer</span><span class="sxs-lookup"><span data-stu-id="c44c8-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="c44c8-104">Указывает версию CTL3D сегодня, которая выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="c44c8-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="c44c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c44c8-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="c44c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c44c8-106">Parameters</span></span>

<span data-ttu-id="c44c8-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c44c8-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c44c8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c44c8-108">Return value</span></span>

<span data-ttu-id="c44c8-109">Возвращает значение, содержащее основной номер версии в байте высокого порядка и дополнительный номер версии в байте нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="c44c8-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="c44c8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c44c8-110">Remarks</span></span>

<span data-ttu-id="c44c8-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c44c8-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c44c8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c44c8-112">Requirements</span></span>



| <span data-ttu-id="c44c8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c44c8-113">Requirement</span></span> | <span data-ttu-id="c44c8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c44c8-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c44c8-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c44c8-115">DLL</span></span><br/> | <dl> <span data-ttu-id="c44c8-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c44c8-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
