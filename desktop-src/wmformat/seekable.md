---
title: Поиска
description: Атрибут, который можно найти, представляет собой атрибут уровня файла, указывающий, может ли приложение искать точки внутри содержимого.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Формат Windows Media с возможностью поиска
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336628"
---
# <a name="seekable"></a><span data-ttu-id="a0c27-104">Поиска</span><span class="sxs-lookup"><span data-stu-id="a0c27-104">Seekable</span></span>

<span data-ttu-id="a0c27-105">Атрибут, который можно **найти** , представляет собой атрибут уровня файла, указывающий, может ли приложение искать точки внутри содержимого.</span><span class="sxs-lookup"><span data-stu-id="a0c27-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a0c27-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="a0c27-106">Global Constant</span></span>

<span data-ttu-id="a0c27-107">g \_ всзвмсикабле</span><span class="sxs-lookup"><span data-stu-id="a0c27-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="a0c27-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a0c27-108">Data Type</span></span>

<span data-ttu-id="a0c27-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="a0c27-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="a0c27-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0c27-110">Remarks</span></span>

<span data-ttu-id="a0c27-111">Это закодированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="a0c27-111">This is a coded attribute.</span></span>

<span data-ttu-id="a0c27-112">Этот атрибут не может дублироваться на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="a0c27-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="a0c27-113">Если этот атрибут используется для отдельного потока, он будет рассматриваться как пользовательские метаданные и не будет передавать его нормальные значения объектам пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a0c27-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="a0c27-114">Значение этого атрибута для файла может различаться в зависимости от того, какой объект предоставляет интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) или [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) , используемый для его извлечения.</span><span class="sxs-lookup"><span data-stu-id="a0c27-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="a0c27-115">Это обусловлено тем, что объекты чтения (синхронные и асинхронные) выполняют более тщательную проверку по сравнению с объектом редактора метаданных, чтобы определить, можно ли перейти к точке в файле.</span><span class="sxs-lookup"><span data-stu-id="a0c27-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="a0c27-116">Значение атрибута для **поиска** , возвращаемое объектом Reader, является более точным.</span><span class="sxs-lookup"><span data-stu-id="a0c27-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0c27-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0c27-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c27-118">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="a0c27-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




