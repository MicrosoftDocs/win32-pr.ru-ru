---
description: Определяет, находится ли сервер терминалов в режиме установки.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Функция Термсрваппинсталлмоде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647966"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="50e29-103">Функция Термсрваппинсталлмоде</span><span class="sxs-lookup"><span data-stu-id="50e29-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="50e29-104">\[Эта функция не поддерживается и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="50e29-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="50e29-105">Он может измениться или исчезнуть полностью без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="50e29-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="50e29-106">Определяет, находится ли сервер терминалов в режиме установки.</span><span class="sxs-lookup"><span data-stu-id="50e29-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e29-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50e29-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="50e29-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50e29-108">Parameters</span></span>

<span data-ttu-id="50e29-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="50e29-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50e29-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50e29-110">Return value</span></span>

<span data-ttu-id="50e29-111">Эта функция возвращает **значение true** , если сервер терминалов находится в режиме установки, и **значение false** , если он находится в режиме выполнения.</span><span class="sxs-lookup"><span data-stu-id="50e29-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e29-112">Требования</span><span class="sxs-lookup"><span data-stu-id="50e29-112">Requirements</span></span>



| <span data-ttu-id="50e29-113">Требование</span><span class="sxs-lookup"><span data-stu-id="50e29-113">Requirement</span></span> | <span data-ttu-id="50e29-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50e29-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e29-115">DLL</span><span class="sxs-lookup"><span data-stu-id="50e29-115">DLL</span></span><br/> | <dl> <span data-ttu-id="50e29-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e29-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




