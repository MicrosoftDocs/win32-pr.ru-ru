---
description: Задает формат выходных данных для декодера.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Свойство Авдеккоммонаутпутформат (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538012"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="98d82-103">Авдеккоммонаутпутформат, свойство</span><span class="sxs-lookup"><span data-stu-id="98d82-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="98d82-104">Задает формат выходных данных для декодера.</span><span class="sxs-lookup"><span data-stu-id="98d82-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="98d82-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="98d82-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="98d82-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="98d82-106">Data type</span></span>

<span data-ttu-id="98d82-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="98d82-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="98d82-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="98d82-108">Property GUID</span></span>

<span data-ttu-id="98d82-109">**КОДЕКАПИ \_ авдеккоммонаутпутформат**</span><span class="sxs-lookup"><span data-stu-id="98d82-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="98d82-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="98d82-110">Property value</span></span>



| <span data-ttu-id="98d82-111">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="98d82-111">GUID</span></span>                                                               | <span data-ttu-id="98d82-112">Описание</span><span class="sxs-lookup"><span data-stu-id="98d82-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d82-113">КОДЕКАПИ \_ GUID \_ авдекаудиуутпутформат \_ PCM</span><span class="sxs-lookup"><span data-stu-id="98d82-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="98d82-114">Звук PCM с использованием любого числа каналов</span><span class="sxs-lookup"><span data-stu-id="98d82-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="98d82-115">КОДЕКАПИ \_ GUID \_ авдекаудиуутпутформат \_ PCM для \_ наушников</span><span class="sxs-lookup"><span data-stu-id="98d82-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="98d82-116">Аудио PCM стерео, с использованием только левой или правой (в наличии/Стро) довнмикс</span><span class="sxs-lookup"><span data-stu-id="98d82-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="98d82-117">\_Автоматический стерео кодекапи GUID \_ авдекаудиуутпутформат \_ PCM \_ \_</span><span class="sxs-lookup"><span data-stu-id="98d82-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="98d82-118">Звук стерео PCM с использованием автоматического выбора режима стерео довнмикс (с конца/ro или lt/RT).</span><span class="sxs-lookup"><span data-stu-id="98d82-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="98d82-119">Это значение можно использовать для звуковых форматов, в которых входной поток определяет предпочтительный режим довнмикс, например Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="98d82-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="98d82-120">КОДЕКАПИ \_ GUID \_ авдекаудиуутпутформат \_ PCM \_ стерео \_ матриксенкодед</span><span class="sxs-lookup"><span data-stu-id="98d82-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="98d82-121">Аудио PCM стерео, использование стерео довнмикс (lt/RT) в кодировке Matrix</span><span class="sxs-lookup"><span data-stu-id="98d82-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="98d82-122">КОДЕКАПИ \_ GUID \_ авдекаудиуутпутформат \_ SPDIF \_ битовый поток</span><span class="sxs-lookup"><span data-stu-id="98d82-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="98d82-123">S/PDIF (формат цифрового интерфейса Sony/Philips) сжатый битовый поток, как определено в IEC-60958</span><span class="sxs-lookup"><span data-stu-id="98d82-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="98d82-124">КОДЕКАПИ \_ GUID \_ авдекаудиуутпутформат \_ SPDIF, \_ PCM</span><span class="sxs-lookup"><span data-stu-id="98d82-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="98d82-125">Стерео PCM S/PDIF, как определено в IEC-60958</span><span class="sxs-lookup"><span data-stu-id="98d82-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="98d82-126">Требования</span><span class="sxs-lookup"><span data-stu-id="98d82-126">Requirements</span></span>



| <span data-ttu-id="98d82-127">Требование</span><span class="sxs-lookup"><span data-stu-id="98d82-127">Requirement</span></span> | <span data-ttu-id="98d82-128">Значение</span><span class="sxs-lookup"><span data-stu-id="98d82-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98d82-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98d82-129">Minimum supported client</span></span><br/> | <span data-ttu-id="98d82-130">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="98d82-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="98d82-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98d82-131">Minimum supported server</span></span><br/> | <span data-ttu-id="98d82-132">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="98d82-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="98d82-133">Header</span><span class="sxs-lookup"><span data-stu-id="98d82-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="98d82-134"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="98d82-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98d82-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98d82-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d82-136">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="98d82-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="98d82-137">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="98d82-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




