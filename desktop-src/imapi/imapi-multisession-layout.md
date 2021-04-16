---
title: Многосеансовый макет IMAPI
description: IMAPI предоставляет разработчикам приложений возможность создавать образы файловой системы ISO 9660 и UDF и записывать их на компакт-диск, DVD-диск и Blu-Ray \ 8482; оптические носители.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104557476"
---
# <a name="imapi-multisession-layout"></a><span data-ttu-id="abac0-103">Многосеансовый макет IMAPI</span><span class="sxs-lookup"><span data-stu-id="abac0-103">IMAPI Multisession Layout</span></span>

<span data-ttu-id="abac0-104">IMAPI предоставляет разработчикам приложений возможность создавать образы файловой системы ISO 9660 и UDF и записывать их на компакт-диски, диски DVD и Blu-Ray™ оптические носители.</span><span class="sxs-lookup"><span data-stu-id="abac0-104">IMAPI provides application developers with the ability to create ISO 9660 and UDF file system images and burn them onto CD, DVD and Blu-Ray™ optical media.</span></span> <span data-ttu-id="abac0-105">В Windows 7 IMAPI обеспечивает дополнительную поддержку для записи в многосеансовую запись на DVD и Blu-Ray™ перезаписываемый носитель.</span><span class="sxs-lookup"><span data-stu-id="abac0-105">With Windows 7, IMAPI provides additional support for multisession burning on DVD and Blu-Ray™ rewritable media.</span></span>

<span data-ttu-id="abac0-106">В следующей документации описана структура диска, используемая IMAPI для реализации многосеансовой связи.</span><span class="sxs-lookup"><span data-stu-id="abac0-106">The following documentation details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="abac0-107">Эти сведения следует использовать для обеспечения взаимодействия между IMAPI и другим программным обеспечением записи, а также для разработчиков этого программного обеспечения, позволяющего создавать многосеансовые образы дисков с поддержкой IMAPI.</span><span class="sxs-lookup"><span data-stu-id="abac0-107">This information should be used to ensure interoperability between IMAPI and other burning software as well as allow the developers of this software to create IMAPI-compatible multisession disc images.</span></span>

> [!Note]  
> <span data-ttu-id="abac0-108">Пример, посвященный созданию многосеансового диска, см. в разделе [Создание диска с многосеансовой](creating-a-multisession-disc.md)информацией.</span><span class="sxs-lookup"><span data-stu-id="abac0-108">For an example detailing the creation of a multisession disc, see [Creating a Multisession Disc](creating-a-multisession-disc.md).</span></span>

 

## <a name="multisession-on-sequential-media"></a><span data-ttu-id="abac0-109">Многосеансы на последовательных носителях</span><span class="sxs-lookup"><span data-stu-id="abac0-109">Multisession on Sequential Media</span></span>

<span data-ttu-id="abac0-110">Реализация многосеансового подключения IMAPI на последовательных носителях поддерживается для использования с носителями CD-R, CD-RW, DVD-R, DVD + R и Blu-Ray™.</span><span class="sxs-lookup"><span data-stu-id="abac0-110">The IMAPI implementation of multisession on sequential media is supported for use with CD-R, CD-RW, DVD-R, DVD+R and Blu-Ray™ media.</span></span> <span data-ttu-id="abac0-111">IMAPI использует режим записи сеанса "на один раз" для CD-RW, и в этом случае формат считается последовательным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="abac0-111">IMAPI uses the Session-At-Once recording mode for CD-RW, and as a result, in this scenario, the format is considered a sequential media type.</span></span>

<span data-ttu-id="abac0-112">В сценарии, включающем многосеансы на последовательных носителях с помощью UDF, IMAPI записывает структуры привязки (указатель на дескриптор тома привязки UDF-АВДП), структуры томов (последовательность дескрипторов UDF) и структуры метаданных файловой системы (дескриптор набора файлов UDF-ФСД) в начале каждого нового сеанса, как описано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="abac0-112">In a scenario involving multisession on sequential media using UDF, IMAPI writes out the anchor structures (UDF Anchor Volume Descriptor Pointer - AVDP), volume structures (UDF Volume Descriptor Sequence - VDS) , and the file system metadata structures (UDF File Set Descriptor - FSD) at the start of every new session as outlined in the following diagram:</span></span>

![Схема, на которой показана структура метаданных файловой системы с точкой подключения "import/F S", обозначенной красной стрелкой на точке привязки физического сеанса 2.](images/multises1.png)

> [!Note]  
> <span data-ttu-id="abac0-114">На этом рисунке показана структура диска IMAPI при использовании UDF 2,50 с избыточными метаданными.</span><span class="sxs-lookup"><span data-stu-id="abac0-114">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="abac0-115">Данные, хранящиеся на последовательных записанных носителях, состоят из нескольких физических сеансов.</span><span class="sxs-lookup"><span data-stu-id="abac0-115">The data stored on sequentially recorded media consists of a number of physical sessions.</span></span> <span data-ttu-id="abac0-116">Каждый сеанс содержит полную файловую систему, представляющую данные пользователя, в виде набора файлов, упорядоченных в каталогах.</span><span class="sxs-lookup"><span data-stu-id="abac0-116">Each session contains a complete file system representing user data as a set of files organized in directories.</span></span> <span data-ttu-id="abac0-117">Метаданные файловой системы состоят из нескольких иерархических структур данных.</span><span class="sxs-lookup"><span data-stu-id="abac0-117">The file system metadata consists of a number of hierarchically organized data structures.</span></span> <span data-ttu-id="abac0-118">В верхней части иерархии находятся структуры привязки (АВДП), расположенные в заранее определенных логических адресах блоков (Лбас).</span><span class="sxs-lookup"><span data-stu-id="abac0-118">At the top of the hierarchy reside anchor structures (AVDP) located at pre-defined Logical Block Addresses (LBAs).</span></span> <span data-ttu-id="abac0-119">Структуры привязки указывают расположения структур следующего уровня, которые не имеют предопределенных адресов.</span><span class="sxs-lookup"><span data-stu-id="abac0-119">The anchor structures specify the locations of the next level structures which do not have predefined addresses.</span></span> <span data-ttu-id="abac0-120">Следующий уровень иерархии после структур привязки содержит структуры томов (VDS), описывающие свойства тома и ссылающиеся на структуры метаданных файловой системы (ФСД), которые, в свою очередь, описывают отдельные файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="abac0-120">The next level of hierarchy after anchor structures contains the volume structures (VDS) that describe the properties of the volume and referencing the file system metadata structures (FSD), which in turn describe individual files and directories.</span></span>

## <a name="multisession-on-rewritable-media"></a><span data-ttu-id="abac0-121">Многосеансы на перезаписываемом носителе</span><span class="sxs-lookup"><span data-stu-id="abac0-121">Multisession on Rewritable Media</span></span>

<span data-ttu-id="abac0-122">Метод последовательного медиа, описанный в предыдущем разделе, несовместим с перезаписываемым (не последовательным) носителем.</span><span class="sxs-lookup"><span data-stu-id="abac0-122">The approach for sequential media outlined in the previous section is incompatible with rewritable (non-sequential) media.</span></span> <span data-ttu-id="abac0-123">Эти форматы мультимедиа включают диски DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ перезаписываемый и другой произвольный носитель, например, Iomega.</span><span class="sxs-lookup"><span data-stu-id="abac0-123">These media formats include DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ rewritable and other random writable media, such as Iomega REV disks.</span></span> <span data-ttu-id="abac0-124">Перезаписываемый носитель не поддерживает концепцию физических сеансов, соответствующих логическим сеансам, которые являются отдельными приращениями, зафиксированными главным приложением.</span><span class="sxs-lookup"><span data-stu-id="abac0-124">Rewritable media does not support the concept of physical sessions corresponding to logical sessions, which are individual increments committed by a mastering application.</span></span> <span data-ttu-id="abac0-125">Предоставляется только один физический сеанс, который является областью, которая начинается с начала диска и представляет всю адресную область, которая может содержать несколько логических сеансов.</span><span class="sxs-lookup"><span data-stu-id="abac0-125">Only a single physical session is exposed, which is an area starting at the beginning of the disc representing the entire addressable area that has the potential to contain multiple logical sessions.</span></span>

> [!Note]  
> <span data-ttu-id="abac0-126">Хотя диск DVD-RW является исключением в том, что он поддерживает концепцию физического сеанса в последовательном режиме, эта возможность в настоящее время не поддерживается IMAPI.</span><span class="sxs-lookup"><span data-stu-id="abac0-126">While DVD-RW is an exception in that it supports the concept of a physical session in the Sequential mode, this capability is currently not supported by IMAPI.</span></span>

 

<span data-ttu-id="abac0-127">Чтобы устранить отсутствие сопоставления "один к одному" между физическими и логическими сеансами в перезаписываемых форматах, IMAPI выборочно обновляет структуры привязки (АВДП) в *первом* логическом сеансе, чтобы они указывали на новые структуры ТОМОВ (VDS) и структуры метаданных файловой системы (ФСД) в начале *последнего* логического сеанса, как описано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="abac0-127">To address the lack of one-to-one mapping between physical and logical sessions on rewritable formats, IMAPI selectively updates the anchor structures (AVDP) in the *first* logical session to point to the new volume structures (VDS) and file system metadata structures (FSD) at the beginning of the *last* logical session as outlined in the following diagram:</span></span>

![Схема, на которой показана структура метаданных файловой системы с "точкой подключения" import/F S ", обозначенной красной стрелкой на" Anchor "логического сеанса 1.](images/multises2.png)

> [!Note]  
> <span data-ttu-id="abac0-129">На этом рисунке показана структура диска IMAPI при использовании UDF 2,50 с избыточными метаданными.</span><span class="sxs-lookup"><span data-stu-id="abac0-129">This figure illustrates the IMAPI disc layout when using UDF 2.50 with redundant metadata.</span></span>

 

<span data-ttu-id="abac0-130">При добавлении нового логического сеанса к перезаписываемому диску IMAPI сначала определяет конец последнего логического сеанса путем анализа метаданных тома (VDS).</span><span class="sxs-lookup"><span data-stu-id="abac0-130">When adding a new logical session to a rewritable disc, IMAPI first determines the end of the last logical session by analyzing the volume metadata (VDS).</span></span> <span data-ttu-id="abac0-131">Затем IMAPI добавляет новый логический сеанс с новыми привязками (АВДП), Volume (VDS) и структурами метаданных файловой системы (ФСД) физически непрерывно с записанным ранее логическим сеансом.</span><span class="sxs-lookup"><span data-stu-id="abac0-131">IMAPI then adds the new logical session, complete with new anchor (AVDP), volume (VDS) and file system metadata structures (FSD), physically contiguous with the previously recorded logical session.</span></span> <span data-ttu-id="abac0-132">На последнем шаге необходимо обновить структуры привязки (АВДП) в начале первого логического сеанса, чтобы они указывали на структуры томов (VDS) в *новом* логическом сеансе.</span><span class="sxs-lookup"><span data-stu-id="abac0-132">The final step requires that the anchor structures (AVDP) at the beginning of the first logical session are updated to point to the volume structures (VDS) in the *new* logical session.</span></span> <span data-ttu-id="abac0-133">Рабочий результат такой же, как и для последовательного носителя.</span><span class="sxs-lookup"><span data-stu-id="abac0-133">The operational result is the same as with sequential media.</span></span>

## <a name="additional-recommendations"></a><span data-ttu-id="abac0-134">Дополнительные рекомендации</span><span class="sxs-lookup"><span data-stu-id="abac0-134">Additional Recommendations</span></span>

-   <span data-ttu-id="abac0-135">**Макет раздела**</span><span class="sxs-lookup"><span data-stu-id="abac0-135">**Partition Layout**</span></span>

    <span data-ttu-id="abac0-136">Для работы с IMAPI совместимости рекомендуется, чтобы разработчики программного обеспечения для записи сторонних разработчиков использовали структуры дисков, описанные в этой документации.</span><span class="sxs-lookup"><span data-stu-id="abac0-136">To achieve IMAPI compatiblity, it is recommended that third-party burning software developers use the disc layouts outlined in this documentation.</span></span> <span data-ttu-id="abac0-137">Разработчикам следует избегать макетов с разделами файловой системы, которые занимают весь диск, так как это требует записи приложений для выявления свободного места в существующих секциях, когда данные необходимо добавить на диск. Часто это достигается благодаря использованию на диске собственных маркеров, указывающих на то, сколько пространства фактически занято данными пользователя.</span><span class="sxs-lookup"><span data-stu-id="abac0-137">Developers should avoid layouts with file system partitions occupying the entire disc, as this requires recording applications to locate free space within existing partitions whenever data needs to be appended to the disc. Oftentimes, the recording applications accomplish this by utilizing proprietary markers on the disc to indicate how much space is actually occupied by user data.</span></span> <span data-ttu-id="abac0-138">Такие структуры дисков несовместимы с IMAPI, так как специальные маркеры не распознаются за пределами приложения, для которого они были созданы.</span><span class="sxs-lookup"><span data-stu-id="abac0-138">Such disc layouts are incompatible with IMAPI as the proprietary markers are not recognized outside of the application they were created for.</span></span>

-   <span data-ttu-id="abac0-139">**Тип секции UDF**</span><span class="sxs-lookup"><span data-stu-id="abac0-139">**UDF Partition Type**</span></span>

    <span data-ttu-id="abac0-140">IMAPI использует тип секции UDF **только для чтения** в своей реализации многосеансовой передачи на записываемом носителе.</span><span class="sxs-lookup"><span data-stu-id="abac0-140">IMAPI uses the **Read-Only** UDF partition type in its implementation of multisession on rewritable media.</span></span> <span data-ttu-id="abac0-141">Разработчики сторонних программ для записи должны использовать тип раздела UDF, предназначенный **только для чтения** , для достижения совместимости с главной записью Windows через IMAPI.</span><span class="sxs-lookup"><span data-stu-id="abac0-141">Developers of third-party burning software should use the **Read-Only** UDF partition type to achieve compatiblity with Windows mastered burning via IMAPI.</span></span> <span data-ttu-id="abac0-142">Если используется другой тип раздела UDF, например, **перезаписываемый** , IMAPI не сможет обеспечить поддержку основных функций.</span><span class="sxs-lookup"><span data-stu-id="abac0-142">If another UDF partition type such as **Rewritable** is used, IMAPI cannot provide mastering support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abac0-143">См. также</span><span class="sxs-lookup"><span data-stu-id="abac0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abac0-144">Создание многосеансового диска</span><span class="sxs-lookup"><span data-stu-id="abac0-144">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)
</dt> <dt>

[<span data-ttu-id="abac0-145">**имултисессионрандомврите**</span><span class="sxs-lookup"><span data-stu-id="abac0-145">**IMultisessionRandomWrite**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




