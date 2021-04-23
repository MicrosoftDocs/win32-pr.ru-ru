---
description: Завершает все необходимые операции в буфере метаданных и освобождает указанный объект Испатиалаудиометадатаитемс.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Метод Испатиалаудиометадатавритер:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142244"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="3e4e7-103">Метод Испатиалаудиометадатавритер:: Close</span><span class="sxs-lookup"><span data-stu-id="3e4e7-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="3e4e7-104">Завершает все необходимые операции в буфере метаданных и освобождает указанный объект [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) .</span><span class="sxs-lookup"><span data-stu-id="3e4e7-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e4e7-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="3e4e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e4e7-106">Parameters</span></span>

<span data-ttu-id="3e4e7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e4e7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e4e7-108">Return value</span></span>

<span data-ttu-id="3e4e7-109">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3e4e7-110">В случае неудачи возможные коды возврата включают, но не ограничиваются значениями, приведенными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="3e4e7-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3e4e7-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="3e4e7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3e4e7-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e4e7-113"><dt>**СПТЛАУД \_ MD \_ клнт \_ E \_ нет \_ \_ открытых элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="3e4e7-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="3e4e7-114">Предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) не был открыт с помощью вызова [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span><span class="sxs-lookup"><span data-stu-id="3e4e7-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="3e4e7-115"><dt>**СПТЛАУД \_ MD \_ клнт \_ E \_ не \_ \_ записано элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="3e4e7-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="3e4e7-116">Не были записаны элементы метаданных в предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span><span class="sxs-lookup"><span data-stu-id="3e4e7-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="3e4e7-117"><dt>**\_элемент сптлауд MD \_ клнт \_ E \_ \_ должен \_ иметь \_ команды**</dt></span><span class="sxs-lookup"><span data-stu-id="3e4e7-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="3e4e7-118">В предоставленный [**испатиалаудиометадатаитемс**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)не записаны команды метаданных.</span><span class="sxs-lookup"><span data-stu-id="3e4e7-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="3e4e7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e4e7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4e7-120">**испатиалаудиометадатавритер**</span><span class="sxs-lookup"><span data-stu-id="3e4e7-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




