---
description: Тип данных ЛАРЖЕИНТ определяет большое \_ целочисленное значение.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: ЛАРЖЕИНТ (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672923"
---
# <a name="largeint"></a><span data-ttu-id="8aa52-103">ларжеинт</span><span class="sxs-lookup"><span data-stu-id="8aa52-103">LARGEINT</span></span>

<span data-ttu-id="8aa52-104">Тип данных **ларжеинт** определяет [**большое \_ целочисленное**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) значение.</span><span class="sxs-lookup"><span data-stu-id="8aa52-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="8aa52-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8aa52-105">Remarks</span></span>

<span data-ttu-id="8aa52-106">Элемент **лпларжеинттабле** структуры [**Set**](set.md) указывает на массив структур **набора** , определяющих одно или несколько значений ларжеинт.</span><span class="sxs-lookup"><span data-stu-id="8aa52-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="8aa52-107">Если **задан этот тип структуры,** сетевой монитор отображает одну из следующих меток с каждым значением ларжеинт, найденным в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="8aa52-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="8aa52-108">Соответствует заданному значению.</span><span class="sxs-lookup"><span data-stu-id="8aa52-108">Matches set value.</span></span> <span data-ttu-id="8aa52-109">Значение ЛАРЖЕИНТ включается в набор.</span><span class="sxs-lookup"><span data-stu-id="8aa52-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="8aa52-110">Неизвестное значение набора.</span><span class="sxs-lookup"><span data-stu-id="8aa52-110">Unknown set value.</span></span> <span data-ttu-id="8aa52-111">Значение ЛАРЖЕИНТ не включено в набор.</span><span class="sxs-lookup"><span data-stu-id="8aa52-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa52-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8aa52-112">Requirements</span></span>



| <span data-ttu-id="8aa52-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8aa52-113">Requirement</span></span> | <span data-ttu-id="8aa52-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8aa52-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa52-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8aa52-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa52-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8aa52-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8aa52-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8aa52-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa52-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8aa52-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8aa52-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8aa52-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa52-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa52-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa52-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8aa52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa52-122">SET</span><span class="sxs-lookup"><span data-stu-id="8aa52-122">SET</span></span>](set.md)
</dt> </dl>

 

