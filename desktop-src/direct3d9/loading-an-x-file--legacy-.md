---
description: Для загрузки файла x используйте следующую процедуру в приложениях прежних версий.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Загрузка файла X (прежних версий) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537028"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="74093-103">Загрузка файла X (прежних версий) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="74093-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="74093-104">Для загрузки файла x используйте следующую процедуру в приложениях прежних версий.</span><span class="sxs-lookup"><span data-stu-id="74093-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="74093-105">Используйте функцию [**директксфилекреате**](directxfilecreate.md) для создания объекта [**идиректксфиле**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="74093-106">Если в файле DirectX есть шаблоны, которые будут загружены, используйте метод [**идиректксфиле:: регистертемплатес**](idirectxfile--registertemplates.md) для регистрации этих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="74093-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="74093-107">Используйте метод [**идиректксфиле:: креатинумобжект**](idirectxfile--createenumobject.md) для создания объекта перечислителя [**идиректксфилинумобжект**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="74093-108">Перебрать объекты в файле.</span><span class="sxs-lookup"><span data-stu-id="74093-108">Loop through the objects in the file.</span></span> <span data-ttu-id="74093-109">Для каждого объекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="74093-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="74093-110">Используйте метод [**идиректксфилинумобжект:: жетнекстдатаобжект**](idirectxfileenumobject--getnextdataobject.md) для получения каждого объекта [**идиректксфиледата**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="74093-111">Используйте метод [**идиректксфиледата:: GetType**](idirectxfiledata--gettype.md) для получения типа данных.</span><span class="sxs-lookup"><span data-stu-id="74093-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="74093-112">Загрузите данные с помощью метода [**идиректксфиледата:: GetData**](idirectxfiledata--getdata.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="74093-113">Если у объекта есть необязательные элементы, извлеките необязательные члены, вызвав метод [**идиректксфиледата:: жетнекстобжект**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="74093-114">Освободите объект [**идиректксфиледата**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="74093-115">Освободите объект [**идиректксфилинумобжект**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="74093-116">Освободите объект [**идиректксфиле**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="74093-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74093-117">См. также</span><span class="sxs-lookup"><span data-stu-id="74093-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74093-118">X-файлы (прежние версии)</span><span class="sxs-lookup"><span data-stu-id="74093-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



