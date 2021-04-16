---
description: Проверяет, могут ли элементы управления использовать объемные эффекты.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Функция Ctl3dEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657831"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="2250b-103">Функция Ctl3dEnabled</span><span class="sxs-lookup"><span data-stu-id="2250b-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="2250b-104">Проверяет, могут ли элементы управления использовать объемные эффекты.</span><span class="sxs-lookup"><span data-stu-id="2250b-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2250b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2250b-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="2250b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2250b-106">Parameters</span></span>

<span data-ttu-id="2250b-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="2250b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2250b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2250b-108">Return value</span></span>

<span data-ttu-id="2250b-109">Возвращает **значение true** , если элементы управления могут использовать трехмерные эффекты; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2250b-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2250b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2250b-110">Remarks</span></span>

<span data-ttu-id="2250b-111">В Windows 4,0 или более поздней версии **Ctl3dEnabled** и [**Ctl3dRegister**](ctl3dregister.md) возвращают **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2250b-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="2250b-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2250b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2250b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2250b-113">Requirements</span></span>



| <span data-ttu-id="2250b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2250b-114">Requirement</span></span> | <span data-ttu-id="2250b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2250b-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2250b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2250b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2250b-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2250b-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
