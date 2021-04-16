---
description: Загрузка файла проекта
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Загрузка файла проекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262380"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="f1f3b-103">Загрузка файла проекта</span><span class="sxs-lookup"><span data-stu-id="f1f3b-103">Loading a Project File</span></span>

<span data-ttu-id="f1f3b-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="f1f3b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f1f3b-105">Чтобы загрузить файл проекта, необходимы два компонента: средство синтаксического анализа XML и пустая временная шкала.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="f1f3b-106">Средство синтаксического анализа XML считывает файл XML-проекта и создает каждый объект, определенный в файле.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="f1f3b-107">Затем он вставляет объекты на временную шкалу и задает все атрибуты временной шкалы, например частоту кадров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="f1f3b-108">В следующем примере кода загружается файл.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="f1f3b-109">Средство синтаксического анализа предоставляет интерфейс [**IXml2Dex**](ixml2dex.md) , который содержит методы для загрузки и сохранения файлов проекта.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="f1f3b-110">Временная шкала предоставляет интерфейс [**иамтимелине**](iamtimeline.md) , который содержит методы для управления временной шкалой и создания новых объектов временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="f1f3b-111">Вызовите функцию **CoCreateInstance** для создания каждого компонента, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="f1f3b-112">Помните, что, создавая новый экземпляр, вы увеличиваете счетчик ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="f1f3b-113">Чтобы избежать утечек памяти, всегда освобождайте интерфейс при работе с ним.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="f1f3b-114">В этом примере указатель на **IXml2Dex** больше не нужен, поэтому интерфейс можно освободить.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="f1f3b-115">Указатель на **иамтимелине** по-прежнему необходим для предварительного просмотра временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="f1f3b-116">Метод [**IXml2Dex:: реадксмлфиле**](ixml2dex-readxmlfile.md) считывает указанный файл и заполняет временную шкалу объектами, определенными в файле.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="f1f3b-117">Имя файла указывается с помощью значения **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="f1f3b-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="f1f3b-118">Чтобы сократить пример, имя файла в примере задается в виде литеральной строки.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="f1f3b-119">Как правило, его можно получить из диалогового окна открытия файла или аналогичного объекта.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="f1f3b-120">Если метод **ReadXml** успешно выполнен, он возвращает код успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="f1f3b-121">В противном случае возвращается код ошибки, такой как VFW \_ E \_ Недопустимый \_ \_ Формат файла.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="f1f3b-122">Всегда проверяйте возвращаемое значение, чтобы правильно обработать состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="f1f3b-123">Опять же, для краткости пример кода не проверяет наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="f1f3b-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1f3b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f1f3b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1f3b-125">Загрузка и предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="f1f3b-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



