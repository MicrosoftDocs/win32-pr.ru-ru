---
description: Кперсистстреам является базовым классом для постоянных свойств фильтров (то есть для фильтрации свойств в сохраненных графах).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Класс Кперсистстреам
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536740"
---
# <a name="cpersiststream-class"></a><span data-ttu-id="196c6-103">Класс Кперсистстреам</span><span class="sxs-lookup"><span data-stu-id="196c6-103">CPersistStream class</span></span>

![Иерархия классов кперсистстреам](images/pstrm01.png)

<span data-ttu-id="196c6-105">`CPersistStream` является базовым классом для постоянных свойств фильтров (то есть для фильтрации свойств в сохраненных графах).</span><span class="sxs-lookup"><span data-stu-id="196c6-105">`CPersistStream` is the base class for persistent properties of filters (that is, filter properties in saved graphs).</span></span>

<span data-ttu-id="196c6-106">Самый простой способ использовать `CPersistStream` :</span><span class="sxs-lookup"><span data-stu-id="196c6-106">The simplest way to use `CPersistStream` is to:</span></span>

1.  <span data-ttu-id="196c6-107">Расположите фильтр для наследования этого класса.</span><span class="sxs-lookup"><span data-stu-id="196c6-107">Arrange for your filter to inherit this class.</span></span>
2.  <span data-ttu-id="196c6-108">Реализуйте [**вритетостреам**](cpersiststream-writetostream.md) и [**реадфромстреам**](cpersiststream-readfromstream.md) в своем классе.</span><span class="sxs-lookup"><span data-stu-id="196c6-108">Implement [**WriteToStream**](cpersiststream-writetostream.md) and [**ReadFromStream**](cpersiststream-readfromstream.md) in your class.</span></span> <span data-ttu-id="196c6-109">Здесь переопределяются функции, которые ничего не делают, но выступают в качестве заполнителей.</span><span class="sxs-lookup"><span data-stu-id="196c6-109">These will override the functions here, which do nothing but act as placeholders.</span></span>
3.  <span data-ttu-id="196c6-110">Измените **нонделегатингкуеринтерфаце** , чтобы он обрабатывал **IPersistStream**.</span><span class="sxs-lookup"><span data-stu-id="196c6-110">Change your **NonDelegatingQueryInterface** to handle **IPersistStream**.</span></span>
4.  <span data-ttu-id="196c6-111">Реализуйте [**сиземакс**](cpersiststream-sizemax.md) , чтобы получить верхнюю границу числа сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="196c6-111">Implement [**SizeMax**](cpersiststream-sizemax.md) to return an upper bound on the number of bytes of data you save.</span></span>

    <span data-ttu-id="196c6-112">При сохранении данных в Юникоде™ следует помнить, что значение WCHAR равно 2 байтам.</span><span class="sxs-lookup"><span data-stu-id="196c6-112">If you save Unicode™ data, remember that a WCHAR is 2 bytes.</span></span>

5.  <span data-ttu-id="196c6-113">При изменении данных вызовите [**сетдирти**](cpersiststream-setdirty.md).</span><span class="sxs-lookup"><span data-stu-id="196c6-113">When your data changes, call [**SetDirty**](cpersiststream-setdirty.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="196c6-114">Номера версий</span><span class="sxs-lookup"><span data-stu-id="196c6-114">Version Numbers</span></span>

<span data-ttu-id="196c6-115">В какой-то момент вы можете изменить или расширить формат данных.</span><span class="sxs-lookup"><span data-stu-id="196c6-115">At some point you might decide to alter or extend the format of your data.</span></span> <span data-ttu-id="196c6-116">После этого вы должны иметь номер версии во всех старых сохраненных потоках, чтобы вы могли указать, что при чтении они представляют старую или новую форму.</span><span class="sxs-lookup"><span data-stu-id="196c6-116">You will then wish you had a version number in all the old saved streams so you can tell, when you read them, whether they represent the old or new form.</span></span> <span data-ttu-id="196c6-117">Чтобы помочь вам, этот класс записывает и считывает номер версии.</span><span class="sxs-lookup"><span data-stu-id="196c6-117">To assist you, this class writes and reads a version number.</span></span> <span data-ttu-id="196c6-118">При записи он вызывает [**жетсофтвареверсион**](cpersiststream-getsoftwareversion.md) , чтобы выполнить запрос как к версии программного обеспечения, используемого в данный момент.</span><span class="sxs-lookup"><span data-stu-id="196c6-118">When it writes, it calls [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) to inquire as to the version of the software being used at the moment.</span></span> <span data-ttu-id="196c6-119">(Фактически это номер версии структуры данных в файле.) Он записывает его в первую очередь на данные.</span><span class="sxs-lookup"><span data-stu-id="196c6-119">(In effect, this is a version number of the data layout in the file.) It writes this as the first thing in the data.</span></span> <span data-ttu-id="196c6-120">Если вы хотите изменить версию, реализуйте (Переопределите) **жетсофтвареверсион**.</span><span class="sxs-lookup"><span data-stu-id="196c6-120">If you want to change the version, implement (override) **GetSoftwareVersion**.</span></span> <span data-ttu-id="196c6-121">Он считывает номер версии из файла в **mPS \_ двфилеверсион** перед вызовом [**Реадфромстреам**](cpersiststream-readfromstream.md), поэтому в **реадфромстреам** можно проверить **mPS \_ двфилеверсион** , чтобы узнать, считывается ли файл старой версии.</span><span class="sxs-lookup"><span data-stu-id="196c6-121">It reads the version number from the file into **mPS\_dwFileVersion** before calling [**ReadFromStream**](cpersiststream-readfromstream.md), so in **ReadFromStream** you can check **mPS\_dwFileVersion** to see if you are reading an old version file.</span></span> <span data-ttu-id="196c6-122">Обычно следует принимать файлы, версия которых не новее версии программного обеспечения, считывающего их.</span><span class="sxs-lookup"><span data-stu-id="196c6-122">Usually you should accept files whose version is no newer than the software version that is reading them.</span></span>

<span data-ttu-id="196c6-123">**Кперсистстреам** реализует [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="196c6-123">**CPersistStream** implements [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="196c6-124">Дополнительные сведения о реализации см. в справочнике по COM в пакете SDK для платформы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="196c6-124">For more implementation information, see the COM Reference in the Microsoft Platform SDK.</span></span>



| <span data-ttu-id="196c6-125">Защищенные члены данных</span><span class="sxs-lookup"><span data-stu-id="196c6-125">Protected Data Members</span></span>                                          | <span data-ttu-id="196c6-126">Описание</span><span class="sxs-lookup"><span data-stu-id="196c6-126">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="196c6-127">mPS \_ двфилеверсион</span><span class="sxs-lookup"><span data-stu-id="196c6-127">mPS\_dwFileVersion</span></span>                                              | <span data-ttu-id="196c6-128">Номер версии файла.</span><span class="sxs-lookup"><span data-stu-id="196c6-128">Version number of the file.</span></span>                                                   |
| <span data-ttu-id="196c6-129">mPS \_ фдирти</span><span class="sxs-lookup"><span data-stu-id="196c6-129">mPS\_fDirty</span></span>                                                     | <span data-ttu-id="196c6-130">Данные для этого потока должны быть сохранены.</span><span class="sxs-lookup"><span data-stu-id="196c6-130">Data for this stream must be saved.</span></span>                                           |
| <span data-ttu-id="196c6-131">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="196c6-131">Member Functions</span></span>                                                | <span data-ttu-id="196c6-132">Описание</span><span class="sxs-lookup"><span data-stu-id="196c6-132">Description</span></span>                                                                   |
| [<span data-ttu-id="196c6-133">**кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="196c6-133">**CPersistStream**</span></span>](cpersiststream-cpersiststream.md)         | <span data-ttu-id="196c6-134">Конструирует объект **кперсистстреам** .</span><span class="sxs-lookup"><span data-stu-id="196c6-134">Constructs a **CPersistStream** object.</span></span>                                       |
| [<span data-ttu-id="196c6-135">**сетдирти**</span><span class="sxs-lookup"><span data-stu-id="196c6-135">**SetDirty**</span></span>](cpersiststream-setdirty.md)                     | <span data-ttu-id="196c6-136">Указывает, что объект должен быть сохранен в потоке.</span><span class="sxs-lookup"><span data-stu-id="196c6-136">Indicates that the object must be saved to the stream.</span></span>                        |
| <span data-ttu-id="196c6-137">Переопределяемые функции элементов</span><span class="sxs-lookup"><span data-stu-id="196c6-137">Overridable Member Functions</span></span>                                    | <span data-ttu-id="196c6-138">Описание</span><span class="sxs-lookup"><span data-stu-id="196c6-138">Description</span></span>                                                                   |
| [<span data-ttu-id="196c6-139">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="196c6-139">**GetClassID**</span></span>](cpersiststream-getclassid.md)                 | <span data-ttu-id="196c6-140">Получает идентификатор класса этого потока.</span><span class="sxs-lookup"><span data-stu-id="196c6-140">Retrieves the class identifier of this stream.</span></span>                                |
| [<span data-ttu-id="196c6-141">**жетсофтвареверсион**</span><span class="sxs-lookup"><span data-stu-id="196c6-141">**GetSoftwareVersion**</span></span>](cpersiststream-getsoftwareversion.md) | <span data-ttu-id="196c6-142">Возвращает номер версии для этого формата файла.</span><span class="sxs-lookup"><span data-stu-id="196c6-142">Retrieves the version number for this file format.</span></span>                            |
| [<span data-ttu-id="196c6-143">**реадфромстреам**</span><span class="sxs-lookup"><span data-stu-id="196c6-143">**ReadFromStream**</span></span>](cpersiststream-readfromstream.md)         | <span data-ttu-id="196c6-144">Считывает данные фильтра из потока.</span><span class="sxs-lookup"><span data-stu-id="196c6-144">Reads the filter's data from the stream.</span></span>                                      |
| [<span data-ttu-id="196c6-145">**сиземакс**</span><span class="sxs-lookup"><span data-stu-id="196c6-145">**SizeMax**</span></span>](cpersiststream-sizemax.md)                       | <span data-ttu-id="196c6-146">Возвращает число байтов, необходимых для данных (не включая номер версии).</span><span class="sxs-lookup"><span data-stu-id="196c6-146">Retrieves the number of bytes needed for data (not including version number).</span></span> |
| [<span data-ttu-id="196c6-147">**вритетостреам**</span><span class="sxs-lookup"><span data-stu-id="196c6-147">**WriteToStream**</span></span>](cpersiststream-writetostream.md)           | <span data-ttu-id="196c6-148">Записывает данные фильтра в поток.</span><span class="sxs-lookup"><span data-stu-id="196c6-148">Writes the filter's data to the stream.</span></span>                                       |
| <span data-ttu-id="196c6-149">Методы IPersistStream</span><span class="sxs-lookup"><span data-stu-id="196c6-149">IPersistStream Methods</span></span>                                          | <span data-ttu-id="196c6-150">Описание</span><span class="sxs-lookup"><span data-stu-id="196c6-150">Description</span></span>                                                                   |
| [<span data-ttu-id="196c6-151">**жетсиземакс**</span><span class="sxs-lookup"><span data-stu-id="196c6-151">**GetSizeMax**</span></span>](cpersiststream-getsizemax.md)                 | <span data-ttu-id="196c6-152">Возвращает число байтов, необходимых для данных (включая номер версии).</span><span class="sxs-lookup"><span data-stu-id="196c6-152">Retrieves the number of bytes needed for data (including version number).</span></span>     |
| [<span data-ttu-id="196c6-153">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="196c6-153">**IsDirty**</span></span>](cpersiststream-isdirty.md)                       | <span data-ttu-id="196c6-154">Проверяет, нужно ли сохранить объект.</span><span class="sxs-lookup"><span data-stu-id="196c6-154">Checks if the object must be saved.</span></span>                                           |
| [<span data-ttu-id="196c6-155">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="196c6-155">**Load**</span></span>](cpersiststream-load.md)                             | <span data-ttu-id="196c6-156">Загружает данные из потока в память.</span><span class="sxs-lookup"><span data-stu-id="196c6-156">Loads the data from the stream into memory.</span></span>                                   |
| [<span data-ttu-id="196c6-157">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="196c6-157">**Save**</span></span>](cpersiststream-save.md)                             | <span data-ttu-id="196c6-158">Сохраняет данные из памяти в поток.</span><span class="sxs-lookup"><span data-stu-id="196c6-158">Saves the data from memory to the stream.</span></span>                                     |



 

 

 
