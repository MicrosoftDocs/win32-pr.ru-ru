---
description: Использование расширенного профиля Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Использование расширенного профиля Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684748"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a><span data-ttu-id="e2692-103">Использование расширенного профиля Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e2692-103">Using the Windows Media Video 9 Advanced Profile</span></span>

<span data-ttu-id="e2692-104">Базовые видеопроцедуры, описанные в разделе [Работа с видео](workingwithvideo.md) , также применяются непосредственно к расширенному профилю Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="e2692-104">The basic video procedures described in the [Working with Video](workingwithvideo.md) section also apply directly to the Windows Media Video 9 Advanced Profile.</span></span> <span data-ttu-id="e2692-105">Никаких специальных процедур не требуется.</span><span class="sxs-lookup"><span data-stu-id="e2692-105">No special procedures are required.</span></span>

<span data-ttu-id="e2692-106">Расширенный профиль Windows Media Video 9 связан с идентификаторами классов CLSID \_ CWMV9EncMediaObject и CLSID \_ квмвдекмедиаобжект.</span><span class="sxs-lookup"><span data-stu-id="e2692-106">The Windows Media Video 9 Advanced Profile is associated with the class identifiers CLSID\_CWMV9EncMediaObject and CLSID\_CWMVDecMediaObject.</span></span> <span data-ttu-id="e2692-107">Значение FOURCC для типов мультимедиа, использующих этот кодек, — "WVC1".</span><span class="sxs-lookup"><span data-stu-id="e2692-107">The FOURCC value for media types using this codec is "WVC1".</span></span>

<span data-ttu-id="e2692-108">Расширенный профиль Windows Media Video 9 поддерживает все общие режимы кодирования, а также чередующиеся кодировки, смешанные, чередующиеся и прогрессивные кодировки, разрешения, отличные от отображаемых, и функции уменьшения диапазона.</span><span class="sxs-lookup"><span data-stu-id="e2692-108">The Windows Media Video 9 Advanced Profile supports all common encoding modes as well interlaced encoding, mixed interlaced and progressive encoding, resolutions that are different than the display, and range reduction features.</span></span> <span data-ttu-id="e2692-109">Другая возможность — возможность хранить метаданные последовательности и кадра в самом побитовом потоке; ранее это требовало использования интерфейса ASF и API модулей обработки данных.</span><span class="sxs-lookup"><span data-stu-id="e2692-109">Another feature is the ability to store sequence and frame metadata in the bit-stream itself; previously this had required use of the ASF and Data Unit Extensions API.</span></span>

<span data-ttu-id="e2692-110">Следующие свойства расширенного профиля Windows Media Video 9, которые можно контролировать с помощью параметров реестра, не имеют соответствующих строк **ипропертибаг** или **ипропертисторе** :</span><span class="sxs-lookup"><span data-stu-id="e2692-110">The following properties of the Windows Media Video 9 Advanced Profile, which can be controlled using registry settings, do not have corresponding **IPropertyBag** or **IPropertyStore** strings:</span></span>

-   <span data-ttu-id="e2692-111">Параметр дкуант.</span><span class="sxs-lookup"><span data-stu-id="e2692-111">Dquant Option.</span></span>
-   <span data-ttu-id="e2692-112">Сила дкуант.</span><span class="sxs-lookup"><span data-stu-id="e2692-112">Dquant Strength.</span></span>
-   <span data-ttu-id="e2692-113">Принудительно перекрытие.</span><span class="sxs-lookup"><span data-stu-id="e2692-113">Force Overlap.</span></span>
-   <span data-ttu-id="e2692-114">Метод стоимости вектора движения.</span><span class="sxs-lookup"><span data-stu-id="e2692-114">Motion Vector Cost Method.</span></span>

## <a name="achieving-optimal-visual-quality"></a><span data-ttu-id="e2692-115">Достижение оптимального визуального качества</span><span class="sxs-lookup"><span data-stu-id="e2692-115">Achieving Optimal Visual Quality</span></span>

<span data-ttu-id="e2692-116">Чтобы обеспечить оптимальное качество визуального изображения для большинства видеоданных с помощью расширенного профиля Windows Media Video 9, можно задать для свойства [мфпкэй \_ компрессионоптимизатионтипе](mfpkey-compressionoptimizationtypeproperty.md) значение 1.</span><span class="sxs-lookup"><span data-stu-id="e2692-116">For most video data, to achieve optimal visual quality using the Windows Media Video 9 Advanced Profile, you can set the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property to 1.</span></span>

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a><span data-ttu-id="e2692-117">О предыдущих кодеках расширенного профиля Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e2692-117">About the Previous Windows Media Video 9 Advanced Profile Codecs</span></span>

<span data-ttu-id="e2692-118">Текущая версия микрокодека расширенного профиля Windows Media Video 9 основана на обществах, посвященных специалистам по продвижении изображений и телевизионным инженерам (SMPTE), для расширенного профиля VC-1 (SMPTE 421M).</span><span class="sxs-lookup"><span data-stu-id="e2692-118">The current version of the Windows Media Video 9 Advanced Profile codec is based on the Society of Motion Picture and Television Engineers (SMPTE) standard for VC-1 (SMPTE 421M) Advanced Profile.</span></span> <span data-ttu-id="e2692-119">Этот кодек заменяет более ранний кодек Windows, который также называется кодеком расширенного профиля Windows Media Video 9, который был идентифицирован с помощью кода FOURCC "ВМВА".</span><span class="sxs-lookup"><span data-stu-id="e2692-119">This codec replaces the earlier codec from Windows also called the Windows Media Video 9 Advanced Profile codec which was identified by the FOURCC code "WMVA".</span></span> <span data-ttu-id="e2692-120">Предыдущая версия кодека VC-1 была реализована до завершения предыдущего стандарта расширенного профиля VC-1 и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2692-120">The previous version of the VC-1 codec was implemented before the VC-1 advanced profile standard was finalized, and is no longer supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2692-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e2692-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2692-122">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="e2692-122">Working with Video</span></span>](workingwithvideo.md)
</dt> 
<dt>

[<span data-ttu-id="e2692-123">Использование дополнительных параметров кодека расширенного профиля Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e2692-123">Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec</span></span>](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



