---
title: WM/Стреамтипеинфо
description: Атрибут WM/Стреамтипеинфо содержит сведения о конфигурации для указанного потока в файле ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Формат Windows Media WM/Стреамтипеинфо
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411702"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="38795-104">WM/Стреамтипеинфо</span><span class="sxs-lookup"><span data-stu-id="38795-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="38795-105">Атрибут **WM/стреамтипеинфо** содержит сведения о конфигурации для указанного потока в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="38795-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="38795-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="38795-106">Global Constant</span></span>

<span data-ttu-id="38795-107">g \_ всзвмстреамтипеинфо</span><span class="sxs-lookup"><span data-stu-id="38795-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="38795-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="38795-108">Data Type</span></span>

<span data-ttu-id="38795-109">[**WM \_ \_ \_ сведения о типе потока**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ \_ двоичный тип ВМТ**)</span><span class="sxs-lookup"><span data-stu-id="38795-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="38795-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38795-110">Remarks</span></span>

<span data-ttu-id="38795-111">Этот атрибут применяется к конкретным потокам.</span><span class="sxs-lookup"><span data-stu-id="38795-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="38795-112">Этот атрибут нельзя получить для потока 0.</span><span class="sxs-lookup"><span data-stu-id="38795-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="38795-113">Этот атрибут доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="38795-113">This attribute is read-only.</span></span>

<span data-ttu-id="38795-114">Доступ к **WM/стреамтипеинфо** можно получить с помощью объекта редактора метаданных.</span><span class="sxs-lookup"><span data-stu-id="38795-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="38795-115">Это единственный способ получить доступ к сведениям о конфигурации потока, не открывая файл с объектом Reader (или синхронным объектом Reader).</span><span class="sxs-lookup"><span data-stu-id="38795-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="38795-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38795-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38795-117">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="38795-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




