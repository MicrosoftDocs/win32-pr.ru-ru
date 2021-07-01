---
title: Иажент Загрузка
description: Иажент Загрузка
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120937"
---
# <a name="iagentload"></a><span data-ttu-id="369c0-103">Иажент:: Load</span><span class="sxs-lookup"><span data-stu-id="369c0-103">IAgent::Load</span></span>

<span data-ttu-id="369c0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="369c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="369c0-105">Загружает символ в коллекцию [**символов**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="369c0-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="369c0-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="369c0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="369c0-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*влоадкэй*</span><span class="sxs-lookup"><span data-stu-id="369c0-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="369c0-108">Тип данных Variant, который должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="369c0-108">A variant datatype that must be one of the following:</span></span>



| <span data-ttu-id="369c0-109">Значение</span><span class="sxs-lookup"><span data-stu-id="369c0-109">Value</span></span>           | <span data-ttu-id="369c0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="369c0-110">Description</span></span>                                                                      |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="369c0-111">*filespec*</span><span class="sxs-lookup"><span data-stu-id="369c0-111">*filespec*</span></span> | <span data-ttu-id="369c0-112">Локальное расположение файла определения указанного символа.</span><span class="sxs-lookup"><span data-stu-id="369c0-112">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="369c0-113">*URL-адрес*</span><span class="sxs-lookup"><span data-stu-id="369c0-113">*URL*</span></span>      | <span data-ttu-id="369c0-114">HTTP-адрес для файла определения символа.</span><span class="sxs-lookup"><span data-stu-id="369c0-114">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="369c0-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*пдвчарид*</span><span class="sxs-lookup"><span data-stu-id="369c0-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="369c0-116">Адрес переменной, которая получает идентификатор символа.</span><span class="sxs-lookup"><span data-stu-id="369c0-116">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="369c0-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="369c0-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="369c0-118">Адрес переменной, которая получает идентификатор запроса на [**загрузку**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="369c0-118">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="369c0-119">Можно загрузить символы из подкаталога Microsoft Agent, указав относительный путь (который не включает двоеточие или символ косой черты).</span><span class="sxs-lookup"><span data-stu-id="369c0-119">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="369c0-120">Это префикс добавляет путь к каталогу символов агента (находится в локализованном каталоге% Windows% \\ мсажент).</span><span class="sxs-lookup"><span data-stu-id="369c0-120">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="369c0-121">Можно также использовать относительный адрес для указания собственного каталога в каталоге символов агента.</span><span class="sxs-lookup"><span data-stu-id="369c0-121">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="369c0-122">Один и тот же символ (символ с одинаковым идентификатором GUID) нельзя загрузить несколько раз из одного соединения.</span><span class="sxs-lookup"><span data-stu-id="369c0-122">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="369c0-123">Аналогичным образом нельзя загрузить символ по умолчанию и другие символы одновременно из одного соединения, так как символ по умолчанию может совпадать с другим символом.</span><span class="sxs-lookup"><span data-stu-id="369c0-123">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="369c0-124">Однако можно создать другое соединение (с помощью CoCreateInstance) и загрузить тот же символ.</span><span class="sxs-lookup"><span data-stu-id="369c0-124">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="369c0-125">Поставщик данных Microsoft Agent поддерживает загрузку символьных данных, хранящихся в виде одного структурированного файла (. ACS) с символьными данными и данными анимации либо в виде отдельных символьных данных (. ACF) и Animation (. АКА) файлы.</span><span class="sxs-lookup"><span data-stu-id="369c0-125">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="369c0-126">Как правило, используйте один структурированный. Файл ACS для загрузки символа, хранящегося на локальном диске или в сети и доступ к которому осуществляется с помощью протокола обычного файла (например, UNC-пути).</span><span class="sxs-lookup"><span data-stu-id="369c0-126">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="369c0-127">Используйте отдельный. ACF и. АКА файлы, если требуется загружать файлы анимации по отдельности с удаленного сайта, к которому они обращаются по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="369c0-127">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="369c0-128">Предмет. Файлы ACS, использующие метод [**Load**](load-method.md) , предоставляют доступ к анимации символа; После загрузки можно использовать метод [**Play**](play-method.md) для анимации символа.</span><span class="sxs-lookup"><span data-stu-id="369c0-128">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="369c0-129">Предмет. ACF файлы, вы также можете использовать метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) для загрузки данных анимации.</span><span class="sxs-lookup"><span data-stu-id="369c0-129">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="369c0-130">Метод **Load** не поддерживает загрузку. Файлы ACS с веб-сайта HTTP.</span><span class="sxs-lookup"><span data-stu-id="369c0-130">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="369c0-131">При загрузке символа символ не отображается автоматически.</span><span class="sxs-lookup"><span data-stu-id="369c0-131">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="369c0-132">Чтобы сделать символ видимым, сначала используйте метод [**Показать**](show-method.md) .</span><span class="sxs-lookup"><span data-stu-id="369c0-132">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 