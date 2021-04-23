---
title: Довнлоадколлектион. Стартдовнлоад, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Стартдовнлоад помещает в очередь загрузку.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- Стартдовнлоад метод Windows Media Player
- Стартдовнлоад метод Windows Media Player, класс Довнлоадколлектион
- Класс Довнлоадколлектион Windows Media Player, метод Стартдовнлоад
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698947"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="a421c-108">Довнлоадколлектион. Стартдовнлоад, метод</span><span class="sxs-lookup"><span data-stu-id="a421c-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="a421c-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="a421c-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a421c-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a421c-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a421c-111">Метод **стартдовнлоад** помещает в очередь загрузку.</span><span class="sxs-lookup"><span data-stu-id="a421c-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a421c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a421c-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="a421c-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="a421c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a421c-114">*саурцеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a421c-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a421c-115">**Строка** , указывающая URL-адрес скачивания.</span><span class="sxs-lookup"><span data-stu-id="a421c-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="a421c-116">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a421c-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a421c-117">**Строка** , указывающая тип загрузки.</span><span class="sxs-lookup"><span data-stu-id="a421c-117">**String** specifying the type of download.</span></span> <span data-ttu-id="a421c-118">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a421c-118">Contains one of the following values.</span></span>



| <span data-ttu-id="a421c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a421c-119">Value</span></span>      | <span data-ttu-id="a421c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a421c-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a421c-121">background</span><span class="sxs-lookup"><span data-stu-id="a421c-121">background</span></span> | <span data-ttu-id="a421c-122">(Windows XP и более поздние версии) Загрузка выполняется в фоновом режиме, как только процессорное время станет доступным.</span><span class="sxs-lookup"><span data-stu-id="a421c-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="a421c-123">Состояния загрузки сохраняются даже при завершении работы проигрывателя Windows Media или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a421c-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="a421c-124">реальное время</span><span class="sxs-lookup"><span data-stu-id="a421c-124">real time</span></span>  | <span data-ttu-id="a421c-125">(Все поддерживаемые операционные системы.) Загрузка выполняется всего один раз.</span><span class="sxs-lookup"><span data-stu-id="a421c-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="a421c-126">Между сеансами не сохраняются состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="a421c-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a421c-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a421c-127">Return value</span></span>

<span data-ttu-id="a421c-128">Этот метод возвращает объект **довнлоадитем** .</span><span class="sxs-lookup"><span data-stu-id="a421c-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a421c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a421c-129">Remarks</span></span>

<span data-ttu-id="a421c-130">При запуске новой загрузки диспетчер загрузки добавляет его как элемент в коллекцию загрузки, которая инициировала скачивание.</span><span class="sxs-lookup"><span data-stu-id="a421c-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="a421c-131">Можно скачать только следующие форматы мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="a421c-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="a421c-132">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="a421c-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="a421c-133">MP3</span><span class="sxs-lookup"><span data-stu-id="a421c-133">MP3</span></span>
-   <span data-ttu-id="a421c-134">Звуковые файлы в формате WMA</span><span class="sxs-lookup"><span data-stu-id="a421c-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="a421c-135">Видеофайлы в формате WMV</span><span class="sxs-lookup"><span data-stu-id="a421c-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="a421c-136">Параметр *саурцеурл* не поддерживает строки в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="a421c-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="a421c-137">Он должен указывать на допустимое содержимое.</span><span class="sxs-lookup"><span data-stu-id="a421c-137">It must point to valid content.</span></span> <span data-ttu-id="a421c-138">Перенаправления не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a421c-138">Redirects are not supported.</span></span>

<span data-ttu-id="a421c-139">При использовании Windows XP звуковые файлы автоматически помещаются в соответствующие **музыкальные** папки на основе значений метаданных на уровне файлов.</span><span class="sxs-lookup"><span data-stu-id="a421c-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="a421c-140">Видеофайлы помещаются в \\ музыкальный \\ файл \\ с типом *случайных чисел* \\ , где *случайное число* — случайное значение, создаваемое проигрывателем Windows Media для каждого пользователя, а *тип* — "реальное время" или "фон", в зависимости от типа скачивания.</span><span class="sxs-lookup"><span data-stu-id="a421c-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="a421c-141">При использовании серии проигрывателя Windows Media 9 с Windows 98 и Windows Millennium Edition (Me) аудио-и видеофайлы помещаются в \\ музыкальный \\ файл \\ скачать тип *случайных чисел* \\ , где *случайное число* — это случайное значение, создаваемое проигрывателем для каждого пользователя, а *тип* — "реальное время" или "фон", в зависимости от типа скачивания.</span><span class="sxs-lookup"><span data-stu-id="a421c-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="a421c-142">Обратите внимание, что файлы могут быть переименованы на основе атрибутов метаданных, содержащихся в файле и правилах, указанных пользователем в диалоговом окне **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="a421c-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="a421c-143">Файлы, которые не содержат метаданные, например **альбом** или **исполнитель**, могут быть перемещены в папки с меткой Неизвестный исполнитель или Неизвестный альбом.</span><span class="sxs-lookup"><span data-stu-id="a421c-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="a421c-144">Требования</span><span class="sxs-lookup"><span data-stu-id="a421c-144">Requirements</span></span>



| <span data-ttu-id="a421c-145">Требование</span><span class="sxs-lookup"><span data-stu-id="a421c-145">Requirement</span></span> | <span data-ttu-id="a421c-146">Значение</span><span class="sxs-lookup"><span data-stu-id="a421c-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a421c-147">Версия</span><span class="sxs-lookup"><span data-stu-id="a421c-147">Version</span></span><br/> | <span data-ttu-id="a421c-148">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a421c-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="a421c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a421c-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="a421c-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a421c-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a421c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a421c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a421c-152">**Объект Довнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="a421c-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="a421c-153">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="a421c-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





