---
description: Описатель изменяемого строкового буфера, который можно использовать для создания HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (HString. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692318"
---
# <a name="hstring_buffer"></a><span data-ttu-id="ba0f1-103">\_БУФЕР HString</span><span class="sxs-lookup"><span data-stu-id="ba0f1-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="ba0f1-104">Описатель изменяемого строкового буфера, который можно использовать для создания [**HString**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="ba0f1-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="ba0f1-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba0f1-105">Remarks</span></span>

<span data-ttu-id="ba0f1-106">**HString \_ BUFFER** представляет строковый буфер, который можно изменить перед преобразованием в неизменяемый [**HString**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="ba0f1-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="ba0f1-107">Вызовите функцию [**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) , чтобы создать **\_ буфер HString**.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="ba0f1-108">Вызовите [**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) , чтобы преобразовать **\_ буфер HString** в неизменяемый [**HString**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="ba0f1-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0f1-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ba0f1-109">Requirements</span></span>



| <span data-ttu-id="ba0f1-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ba0f1-110">Requirement</span></span> | <span data-ttu-id="ba0f1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ba0f1-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0f1-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba0f1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0f1-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ba0f1-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="ba0f1-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba0f1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0f1-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba0f1-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ba0f1-116">Header</span><span class="sxs-lookup"><span data-stu-id="ba0f1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0f1-117"><dt>HString. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0f1-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0f1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba0f1-118">See also</span></span>

<dl> <span data-ttu-id="ba0f1-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ba0f1-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ba0f1-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="ba0f1-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="ba0f1-121">**виндовспреаллокатестрингбуффер**</span><span class="sxs-lookup"><span data-stu-id="ba0f1-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="ba0f1-122">**виндовспромотестрингбуффер**</span><span class="sxs-lookup"><span data-stu-id="ba0f1-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
