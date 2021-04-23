---
title: WM/Енкодингтиме
description: Атрибут WM/Енкодингтиме содержит метку времени, в которую было закодировано содержимое.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Формат Windows Media WM/Енкодингтиме
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069189"
---
# <a name="wmencodingtime"></a><span data-ttu-id="21106-104">WM/Енкодингтиме</span><span class="sxs-lookup"><span data-stu-id="21106-104">WM/EncodingTime</span></span>

<span data-ttu-id="21106-105">Атрибут **WM/енкодингтиме** содержит метку времени, в которую было закодировано содержимое.</span><span class="sxs-lookup"><span data-stu-id="21106-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="21106-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="21106-106">Global Constant</span></span>

<span data-ttu-id="21106-107">g \_ всзвменкодингтиме</span><span class="sxs-lookup"><span data-stu-id="21106-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="21106-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="21106-108">Data Type</span></span>

<span data-ttu-id="21106-109">**fileTime** (**тип ВМТ, \_ \_ QWORD**)</span><span class="sxs-lookup"><span data-stu-id="21106-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="21106-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21106-110">Remarks</span></span>

<span data-ttu-id="21106-111">Этот атрибут использует значение FILETIME, которое представляет собой 64-разрядное значение, представляющее число единиц времени 100-наносекундных, истекших с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="21106-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="21106-112">Дополнительные сведения о параметре FILETIME см. в разделе "сведения о системе Windows" пакета Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="21106-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="21106-113">Этот атрибут не является закодированным.</span><span class="sxs-lookup"><span data-stu-id="21106-113">This is not a coded attribute.</span></span> <span data-ttu-id="21106-114">Его необходимо задать вручную, если вы хотите включить его в файлы.</span><span class="sxs-lookup"><span data-stu-id="21106-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="21106-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21106-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21106-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="21106-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




