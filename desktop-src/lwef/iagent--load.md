---
title: Иажент Загрузка
description: Иажент Загрузка
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987488"
---
# <a name="iagentload"></a><span data-ttu-id="a9635-103">Иажент:: Load</span><span class="sxs-lookup"><span data-stu-id="a9635-103">IAgent::Load</span></span>

<span data-ttu-id="a9635-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9635-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="a9635-105">Загружает символ в коллекцию [**символов**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="a9635-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="a9635-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a9635-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a9635-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*влоадкэй*</span><span class="sxs-lookup"><span data-stu-id="a9635-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="a9635-108">Тип данных Variant, который должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="a9635-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a9635-109">*filespec*</span><span class="sxs-lookup"><span data-stu-id="a9635-109">*filespec*</span></span> | <span data-ttu-id="a9635-110">Локальное расположение файла определения указанного символа.</span><span class="sxs-lookup"><span data-stu-id="a9635-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="a9635-111">*URL-адрес*</span><span class="sxs-lookup"><span data-stu-id="a9635-111">*URL*</span></span>      | <span data-ttu-id="a9635-112">HTTP-адрес для файла определения символа.</span><span class="sxs-lookup"><span data-stu-id="a9635-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="a9635-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*пдвчарид*</span><span class="sxs-lookup"><span data-stu-id="a9635-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a9635-114">Адрес переменной, которая получает идентификатор символа.</span><span class="sxs-lookup"><span data-stu-id="a9635-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="a9635-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="a9635-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="a9635-116">Адрес переменной, которая получает идентификатор запроса на [**загрузку**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a9635-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="a9635-117">Можно загрузить символы из подкаталога Microsoft Agent, указав относительный путь (который не включает двоеточие или символ косой черты).</span><span class="sxs-lookup"><span data-stu-id="a9635-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="a9635-118">Это префикс добавляет путь к каталогу символов агента (находится в локализованном каталоге% Windows% \\ мсажент).</span><span class="sxs-lookup"><span data-stu-id="a9635-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="a9635-119">Можно также использовать относительный адрес для указания собственного каталога в каталоге символов агента.</span><span class="sxs-lookup"><span data-stu-id="a9635-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="a9635-120">Один и тот же символ (символ с одинаковым идентификатором GUID) нельзя загрузить несколько раз из одного соединения.</span><span class="sxs-lookup"><span data-stu-id="a9635-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="a9635-121">Аналогичным образом нельзя загрузить символ по умолчанию и другие символы одновременно из одного соединения, так как символ по умолчанию может совпадать с другим символом.</span><span class="sxs-lookup"><span data-stu-id="a9635-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="a9635-122">Однако можно создать другое соединение (с помощью CoCreateInstance) и загрузить тот же символ.</span><span class="sxs-lookup"><span data-stu-id="a9635-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="a9635-123">Поставщик данных Microsoft Agent поддерживает загрузку символьных данных, хранящихся в виде одного структурированного файла (. ACS) с символьными данными и данными анимации либо в виде отдельных символьных данных (. ACF) и Animation (. АКА) файлы.</span><span class="sxs-lookup"><span data-stu-id="a9635-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="a9635-124">Как правило, используйте один структурированный. Файл ACS для загрузки символа, хранящегося на локальном диске или в сети и доступ к которому осуществляется с помощью протокола обычного файла (например, UNC-пути).</span><span class="sxs-lookup"><span data-stu-id="a9635-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="a9635-125">Используйте отдельный. ACF и. АКА файлы, если требуется загружать файлы анимации по отдельности с удаленного сайта, к которому они обращаются по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="a9635-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="a9635-126">Предмет. Файлы ACS, использующие метод [**Load**](load-method.md) , предоставляют доступ к анимации символа; После загрузки можно использовать метод [**Play**](play-method.md) для анимации символа.</span><span class="sxs-lookup"><span data-stu-id="a9635-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="a9635-127">Предмет. ACF файлы, вы также можете использовать метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) для загрузки данных анимации.</span><span class="sxs-lookup"><span data-stu-id="a9635-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="a9635-128">Метод **Load** не поддерживает загрузку. Файлы ACS с веб-сайта HTTP.</span><span class="sxs-lookup"><span data-stu-id="a9635-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="a9635-129">При загрузке символа символ не отображается автоматически.</span><span class="sxs-lookup"><span data-stu-id="a9635-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="a9635-130">Чтобы сделать символ видимым, сначала используйте метод [**Показать**](show-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a9635-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 