---
title: Обработка событий индивидуализации
description: Обработка событий индивидуализации
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Пакет SDK для Windows Media Format, обработка событий индивидуализации
- Пакет SDK для Windows Media Format, события индивидуализации
- Расширенный системный формат (ASF), обработка событий индивидуализации
- ASF (Расширенный системный формат), обработка событий индивидуализации
- Расширенный системный формат (ASF), события индивидуализации
- ASF (Расширенный системный формат), события индивидуализации
- Управление цифровыми правами (DRM), обработка событий индивидуализации
- DRM (Управление цифровыми правами), обработка событий индивидуализации
- Управление цифровыми правами (DRM), события индивидуализации
- DRM (Управление цифровыми правами), события индивидуализации
- события индивидуализации
- события, индивидуальные события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691449"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="be80f-115">Обработка событий индивидуализации</span><span class="sxs-lookup"><span data-stu-id="be80f-115">Handling Individualization Events</span></span>

<span data-ttu-id="be80f-116">Когда приложение с поддержкой DRM пытается открыть защищенный файл, компонент DRM проверяет атрибут [**DRM \_ дрмхеадер \_ индивидуализедверсион**](drm-drmheader-individualizedversion.md) в файле, который указывает минимальный уровень версии, необходимый для доступа к содержимому.</span><span class="sxs-lookup"><span data-stu-id="be80f-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="be80f-117">Все уровни компонента DRM работают со всеми 7,0 и более поздними версиями проигрывателя Windows Media и Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="be80f-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="be80f-118">Если уровень отдельных версий компонента DRM меньше требуемой версии, компонент DRM отправит событие **ВМТ \_ требуется \_ индивидуально** в метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) приложения.</span><span class="sxs-lookup"><span data-stu-id="be80f-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="be80f-119">После этого приложение должно отобразить сообщение или диалоговое окно, предлагающее пользователям либо запустить, либо отменить обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="be80f-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="be80f-120">Этот запрос необходим, поскольку в целях обеспечения конфиденциальности пользователи должны предоставить свое разрешение до установки обновления безопасности на компьютере.</span><span class="sxs-lookup"><span data-stu-id="be80f-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="be80f-121">В заголовке содержимого указаны только первые две цифры для DRM \_ дрмверсион \_ индивидуализедверсион.</span><span class="sxs-lookup"><span data-stu-id="be80f-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="be80f-122">Иными словами, для запроса компонента DRM уровня 2.2.0.1 заголовок будет содержать значение "2,2".</span><span class="sxs-lookup"><span data-stu-id="be80f-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="be80f-123">Чтобы запустить обновление безопасности и/или выполнить индивидуальную настройку, вызовите метод [**ивмдрмреадер:: индивидуализируйте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) с параметром *dwFlags* , равным 1.</span><span class="sxs-lookup"><span data-stu-id="be80f-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="be80f-124">Необходимо выполнить обработку события **ВМТ \_ индивидуализируйте** в приложении.</span><span class="sxs-lookup"><span data-stu-id="be80f-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="be80f-125">Это событие будет запускаться несколько раз компонентом DRM с состоянием процесса индивидуализации, указанным в параметре *pValue* , который приводится к указателю на структуру [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="be80f-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="be80f-126">После успешного создания компонента DRM приложение получит событие **ВМТ \_ без \_ прав \_** , указывающее, что приложение теперь может получить лицензию на содержимое.</span><span class="sxs-lookup"><span data-stu-id="be80f-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="be80f-127">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="be80f-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="be80f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="be80f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be80f-129">**Обработка событий приобретения лицензий**</span><span class="sxs-lookup"><span data-stu-id="be80f-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="be80f-130">**Приложения DRM индивидуализинг**</span><span class="sxs-lookup"><span data-stu-id="be80f-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="be80f-131">**Интерфейс Ивмдрмреадер**</span><span class="sxs-lookup"><span data-stu-id="be80f-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




