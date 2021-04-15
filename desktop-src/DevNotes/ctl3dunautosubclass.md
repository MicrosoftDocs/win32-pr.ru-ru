---
description: Отключает автоматическое подклассы.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Функция Ctl3dUnAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649032"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="f1818-103">Функция Ctl3dUnAutoSubclass</span><span class="sxs-lookup"><span data-stu-id="f1818-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="f1818-104">Отключает автоматическое подклассы.</span><span class="sxs-lookup"><span data-stu-id="f1818-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1818-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1818-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="f1818-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1818-106">Parameters</span></span>

<span data-ttu-id="f1818-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="f1818-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1818-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1818-108">Return value</span></span>

<span data-ttu-id="f1818-109">Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f1818-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1818-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1818-110">Remarks</span></span>

<span data-ttu-id="f1818-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f1818-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1818-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f1818-112">Requirements</span></span>



| <span data-ttu-id="f1818-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f1818-113">Requirement</span></span> | <span data-ttu-id="f1818-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f1818-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1818-115">DLL</span><span class="sxs-lookup"><span data-stu-id="f1818-115">DLL</span></span><br/> | <dl> <span data-ttu-id="f1818-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1818-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
