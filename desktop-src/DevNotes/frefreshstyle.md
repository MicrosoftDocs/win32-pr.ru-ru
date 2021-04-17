---
description: Перезагрузка параметров цвета из реестра.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Функция Фрефрешстиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657267"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="bf18d-103">Функция Фрефрешстиле</span><span class="sxs-lookup"><span data-stu-id="bf18d-103">FRefreshStyle function</span></span>

<span data-ttu-id="bf18d-104">Перезагрузка параметров цвета из реестра.</span><span class="sxs-lookup"><span data-stu-id="bf18d-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf18d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf18d-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="bf18d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf18d-106">Parameters</span></span>

<span data-ttu-id="bf18d-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bf18d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf18d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf18d-108">Return value</span></span>

<span data-ttu-id="bf18d-109">Возвращает значение TRUE в случае успешного выполнения; в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf18d-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf18d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf18d-110">Remarks</span></span>

<span data-ttu-id="bf18d-111">Эта функция не связана с библиотекой импорта или файлом заголовка. Он должен вызываться с помощью функций [**LoadLibrary**](-loadlibrary.md) и [**GetProcAddress**](-getprocaddress-.md) .</span><span class="sxs-lookup"><span data-stu-id="bf18d-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf18d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="bf18d-112">Requirements</span></span>



| <span data-ttu-id="bf18d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="bf18d-113">Requirement</span></span> | <span data-ttu-id="bf18d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bf18d-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf18d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="bf18d-115">DLL</span></span><br/> | <dl> <span data-ttu-id="bf18d-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf18d-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf18d-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf18d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf18d-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="bf18d-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="bf18d-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="bf18d-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




