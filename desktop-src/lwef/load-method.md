---
title: Метод загрузки
description: Метод загрузки
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700855"
---
# <a name="load-method"></a><span data-ttu-id="e78f1-103">Метод загрузки</span><span class="sxs-lookup"><span data-stu-id="e78f1-103">Load Method</span></span>

<span data-ttu-id="e78f1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e78f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e78f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e78f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e78f1-106">Загружает символ в коллекцию [**символов**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="e78f1-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="e78f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e78f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e78f1-108">\*Агент ***. Символы. Load "*** чарактерид \* \* *",* \*  *поставщик*</span><span class="sxs-lookup"><span data-stu-id="e78f1-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="e78f1-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="e78f1-109">Part</span></span>          | <span data-ttu-id="e78f1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e78f1-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78f1-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="e78f1-111">*CharacterID*</span></span> | <span data-ttu-id="e78f1-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e78f1-112">Required.</span></span> <span data-ttu-id="e78f1-113">Строковое значение, которое будет использоваться для ссылки на символьные данные для загрузки.</span><span class="sxs-lookup"><span data-stu-id="e78f1-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="e78f1-114">*Поставщик*</span><span class="sxs-lookup"><span data-stu-id="e78f1-114">*Provider*</span></span>    | <span data-ttu-id="e78f1-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="e78f1-115">Required.</span></span> <span data-ttu-id="e78f1-116">Тип данных Variant, который должен быть одним из следующих: **filespec** расположение локального файла для указанного файла определения символа.</span><span class="sxs-lookup"><span data-stu-id="e78f1-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="e78f1-117">**URL-адрес** HTTP-адрес для файла определения символа.</span><span class="sxs-lookup"><span data-stu-id="e78f1-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e78f1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e78f1-118">Remarks</span></span>

<span data-ttu-id="e78f1-119">Можно загрузить символы из подкаталога агента, указав относительный путь (который не включает двоеточие или символ косой черты).</span><span class="sxs-lookup"><span data-stu-id="e78f1-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="e78f1-120">Это префикс добавляет путь к каталогу символов агента (находится в локализованном каталоге Windows \\ мсажент).</span><span class="sxs-lookup"><span data-stu-id="e78f1-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="e78f1-121">Например, при указании следующего параметра будет загружен Genie. ACS из каталога chars агента:</span><span class="sxs-lookup"><span data-stu-id="e78f1-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="e78f1-122">Можно также указать собственный каталог в каталоге chars агента.</span><span class="sxs-lookup"><span data-stu-id="e78f1-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="e78f1-123">Можно загрузить символ, заданный в качестве символа по умолчанию текущего пользователя, не включая путь в качестве второго параметра метода **Load** .</span><span class="sxs-lookup"><span data-stu-id="e78f1-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="e78f1-124">Один и тот же символ (символ с одинаковым идентификатором GUID) нельзя загрузить несколько раз из одного экземпляра элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e78f1-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="e78f1-125">Аналогичным образом нельзя одновременно загрузить символ по умолчанию и другие символы из одного экземпляра элемента управления, поскольку символ по умолчанию может совпадать с другим символом.</span><span class="sxs-lookup"><span data-stu-id="e78f1-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="e78f1-126">Если вы попытаетесь сделать это, сервер выдаст ошибку.</span><span class="sxs-lookup"><span data-stu-id="e78f1-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="e78f1-127">Однако можно создать другой экземпляр элемента управления агента и загрузить тот же символ.</span><span class="sxs-lookup"><span data-stu-id="e78f1-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="e78f1-128">Поставщик данных Microsoft Agent поддерживает загрузку символьных данных, хранящихся либо в виде одного структурированного файла (. ACS) с символьными данными и данными анимации вместе или в виде отдельных символьных данных (. ACF) и Animation (. АКА) файлы.</span><span class="sxs-lookup"><span data-stu-id="e78f1-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="e78f1-129">Используйте один структурированный. Файл ACS для загрузки символа, хранящегося на локальном диске или в сети и доступ к которому осуществляется с помощью обычного файлового протокола (например, UNC-пути).</span><span class="sxs-lookup"><span data-stu-id="e78f1-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="e78f1-130">Используйте отдельный. ACF и. АКА файлы, если требуется загружать файлы анимации по отдельности с удаленного сайта, к которому они обращаются по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="e78f1-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="e78f1-131">Предмет. Файлы ACS, использующие метод **Load** , обеспечивают доступ к анимации символа.</span><span class="sxs-lookup"><span data-stu-id="e78f1-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="e78f1-132">Предмет. ACF файлы, для загрузки данных анимации также используется метод [**Get**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e78f1-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="e78f1-133">Метод **Load** не поддерживает загрузку. Файлы ACS с веб-сайта HTTP.</span><span class="sxs-lookup"><span data-stu-id="e78f1-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="e78f1-134">При загрузке символа символ не отображается автоматически.</span><span class="sxs-lookup"><span data-stu-id="e78f1-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="e78f1-135">Чтобы сделать символ видимым, сначала используйте метод [**Показать**](show-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e78f1-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="e78f1-136">Если метод **Load** используется для загрузки символьного файла, хранящегося на локальном компьютере, и вызов завершается с ошибкой; Например, поскольку файл не найден, агент вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e78f1-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="e78f1-137">Вы можете использовать поддержку на языке программирования, чтобы предоставить подпрограмму обработки ошибок для перехвата и обработки ошибки.</span><span class="sxs-lookup"><span data-stu-id="e78f1-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="e78f1-138">Можно также решить эту ошибку, установив для [**Раисерекуестеррорс**](https://www.bing.com/search?q=**RaiseRequestErrors**) **значение false**, объявляя объект и назначив ему запрос на **загрузку** .</span><span class="sxs-lookup"><span data-stu-id="e78f1-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="e78f1-139">Затем выполните вызов **Load** с инструкцией, которая проверяет состояние объекта [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="e78f1-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="e78f1-140">При загрузке нелокального символа; Например, при использовании протокола HTTP можно также проверить сбой **загрузки** , назначив объект [**запроса**](/windows/desktop/lwef/the-request-object) методу **Load** .</span><span class="sxs-lookup"><span data-stu-id="e78f1-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="e78f1-141">Однако, поскольку этот метод загрузки символа обрабатывается асинхронно, проверьте его состояние в событии [**рекуесткомплете**](requestcomplete-event.md) .</span><span class="sxs-lookup"><span data-stu-id="e78f1-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="e78f1-142">Этот метод не будет работать при загрузке символа с помощью протокола UNC, так как метод **Load** обрабатывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="e78f1-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

