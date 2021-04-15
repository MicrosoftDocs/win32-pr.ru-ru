---
UID: ''
title: Функция Гуардчекклонгжумптаржет
description: Пытается проверить, является ли целевой объект longjmp допустимым.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105654277"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="dd8c9-103">Функция Гуардчекклонгжумптаржет</span><span class="sxs-lookup"><span data-stu-id="dd8c9-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="dd8c9-104">Описание</span><span class="sxs-lookup"><span data-stu-id="dd8c9-104">Description</span></span>

<span data-ttu-id="dd8c9-105">Пытается проверить, является ли целевой объект [longjmp](/cpp/c-runtime-library/reference/longjmp) допустимым для процесса, в котором включена [Защита потока управления (cfg)](../secbp/control-flow-guard.md) .</span><span class="sxs-lookup"><span data-stu-id="dd8c9-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="dd8c9-106">Если целевой адрес соответствует сопоставлению изображений, то для двоичного файла извлекаются допустимые целевые объекты.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="dd8c9-107">Функция использует эти целевые объекты для проверки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="dd8c9-108">Если двоичный файл не имеет метаданных, описывающих набор допустимых целевых объектов *longjmp* , функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="dd8c9-109">Если целевой адрес соответствует сопоставлению без образов, как в JIT-коде, для определения того, разрешен ли переход, используется глобальная политика только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd8c9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd8c9-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="dd8c9-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="dd8c9-111">TargetAddress [in]</span></span>

<span data-ttu-id="dd8c9-112">Целевой адрес для перехода.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="dd8c9-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="dd8c9-113">Flags [in]</span></span>

<span data-ttu-id="dd8c9-114">Флаги, описывающие операцию, которая должна быть выполнена с адресом.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="dd8c9-115">Если указать **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), эта функция не прерывает процесс, если целевой объект является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="dd8c9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd8c9-116">Returns</span></span>

<span data-ttu-id="dd8c9-117">**Значение true** , если целевой объект является допустимым; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dd8c9-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8c9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd8c9-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="dd8c9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd8c9-119">See also</span></span>
