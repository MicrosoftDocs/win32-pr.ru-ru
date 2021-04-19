---
description: Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.
title: Функция Длпмустпастефромсистемклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495917"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="1274e-103">Функция Длпмустпастефромсистемклипбоард</span><span class="sxs-lookup"><span data-stu-id="1274e-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="1274e-104">Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.</span><span class="sxs-lookup"><span data-stu-id="1274e-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="1274e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1274e-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="1274e-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1274e-106">Return value</span></span>

<span data-ttu-id="1274e-107">Значение TRUE, если вызов в буфер обмена ОС является обязательным; в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="1274e-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1274e-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="1274e-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1274e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1274e-109">Requirements</span></span>



| <span data-ttu-id="1274e-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1274e-110">Requirement</span></span>          |    <span data-ttu-id="1274e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1274e-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1274e-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1274e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1274e-113">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="1274e-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1274e-114">DLL</span><span class="sxs-lookup"><span data-stu-id="1274e-114">DLL</span></span><br/>                      | <span data-ttu-id="1274e-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1274e-115">EndpointDlp.dll</span></span> |