---
description: Реализация этого интерфейса предоставляется в виде образца кода с помощью пакета SDK DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Интерфейс IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672973"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="5814d-103">Интерфейс IMpeg2PsiParser</span><span class="sxs-lookup"><span data-stu-id="5814d-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="5814d-104">Реализация этого интерфейса предоставляется в виде образца кода с помощью пакета SDK DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5814d-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="5814d-105">Это не поддерживаемый API-интерфейс DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5814d-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="5814d-106">`IMpeg2PsiParser`Интерфейс извлекает сведения о программе (PSI) из фильтра средства синтаксического анализа PSI, который предоставляется в пакете SDK DirectShow в качестве образца фильтра.</span><span class="sxs-lookup"><span data-stu-id="5814d-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="5814d-107">Приложение может использовать этот фильтр для отображения идентификаторов программ (PID) в фильтре демультиплексора MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5814d-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="5814d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5814d-108">Members</span></span>

<span data-ttu-id="5814d-109">Интерфейс **IMpeg2PsiParser** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5814d-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5814d-110">**IMpeg2PsiParser** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5814d-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="5814d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5814d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5814d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5814d-112">Methods</span></span>

<span data-ttu-id="5814d-113">Интерфейс **IMpeg2PsiParser** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5814d-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="5814d-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5814d-114">Method</span></span>                                                                             | <span data-ttu-id="5814d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5814d-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="5814d-116">[**финдрекордпрограммаппид**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5814d-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="5814d-117">Находит идентификатор таблицы схемы программы (ПЛТ) для программы с учетом номера программы.</span><span class="sxs-lookup"><span data-stu-id="5814d-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="5814d-118">**жеткаунтофелементаристреамс**</span><span class="sxs-lookup"><span data-stu-id="5814d-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="5814d-119">Возвращает количество простейших потоков в указанной программе.</span><span class="sxs-lookup"><span data-stu-id="5814d-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="5814d-120">**жеткаунтофпрограмс**</span><span class="sxs-lookup"><span data-stu-id="5814d-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="5814d-121">Возвращает количество программ в транспортном потоке.</span><span class="sxs-lookup"><span data-stu-id="5814d-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="5814d-122">**жетпатверсионнумбер**</span><span class="sxs-lookup"><span data-stu-id="5814d-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="5814d-123">Извлекает \_ поле номера версии из таблицы взаимосвязей программ (PAT).</span><span class="sxs-lookup"><span data-stu-id="5814d-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="5814d-124">**жетпмтверсионнумбер**</span><span class="sxs-lookup"><span data-stu-id="5814d-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="5814d-125">Извлекает \_ поле номера версии из указанного типа ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="5814d-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="5814d-126">[**жетрекорделементарипид**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5814d-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="5814d-127">Получает назначение PID для указанного простейшего потока в программе.</span><span class="sxs-lookup"><span data-stu-id="5814d-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="5814d-128">[**жетрекордпрограммаппид**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5814d-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="5814d-129">Получает назначение PID для указанного типа ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="5814d-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="5814d-130">**жетрекордпрограмнумбер**</span><span class="sxs-lookup"><span data-stu-id="5814d-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="5814d-131">Возвращает номер программы для указанной программы.</span><span class="sxs-lookup"><span data-stu-id="5814d-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="5814d-132">[**жетрекордстреамтипе**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5814d-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="5814d-133">Извлекает тип потока для указанного простейшего потока в программе.</span><span class="sxs-lookup"><span data-stu-id="5814d-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="5814d-134">**жеттранспортстреамид**</span><span class="sxs-lookup"><span data-stu-id="5814d-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="5814d-135">Получает поле идентификатора транспортного \_ потока \_ из Pat.</span><span class="sxs-lookup"><span data-stu-id="5814d-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="5814d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5814d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5814d-137">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="5814d-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
