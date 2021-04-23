---
title: Структуры подключаемых модулей
description: Структуры для разработки клиентских приложений с помощью API биометрическая платформа Windows.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API биометрическая платформа Windows API биометрическая платформа Windows, структуры подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331672"
---
# <a name="plug-in-structures"></a><span data-ttu-id="45b6d-104">Структуры подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="45b6d-104">Plug-in Structures</span></span>

<span data-ttu-id="45b6d-105">Для разработки клиентских приложений с помощью биометрическая платформа Windows API поддерживаются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="45b6d-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="45b6d-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="45b6d-106">In this section</span></span>



| <span data-ttu-id="45b6d-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="45b6d-107">Topic</span></span>                                                                                                | <span data-ttu-id="45b6d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="45b6d-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45b6d-109">**\_Политика учетных записей винбио \_**</span><span class="sxs-lookup"><span data-stu-id="45b6d-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="45b6d-110">Содержит политику антиподмены по умолчанию или учетную запись.</span><span class="sxs-lookup"><span data-stu-id="45b6d-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="45b6d-111">**\_ \_ версия интерфейса адаптера \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="45b6d-112">Содержит основной и дополнительный номер версии, используемые в таблицах интерфейса модуля, датчика и адаптера хранилища.</span><span class="sxs-lookup"><span data-stu-id="45b6d-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="45b6d-113">**\_интерфейс ядра \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="45b6d-114">Содержит указатели на функции пользовательского адаптера подсистемы.</span><span class="sxs-lookup"><span data-stu-id="45b6d-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="45b6d-115">**ВИНБИО \_ Расширенные \_ Параметры регистрации \_**</span><span class="sxs-lookup"><span data-stu-id="45b6d-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="45b6d-116">Содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации.</span><span class="sxs-lookup"><span data-stu-id="45b6d-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="45b6d-117">**\_конвейер винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="45b6d-118">Содержит общие контекстные сведения, используемые компонентами датчика, подсистемы и адаптера хранилища в одном биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="45b6d-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="45b6d-119">**\_интерфейс датчика \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="45b6d-120">Содержит указатели на функции пользовательского адаптера датчика.</span><span class="sxs-lookup"><span data-stu-id="45b6d-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="45b6d-121">**\_интерфейс хранилища \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="45b6d-122">Содержит указатели на пользовательские функции адаптера хранилища.</span><span class="sxs-lookup"><span data-stu-id="45b6d-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="45b6d-123">**\_запись хранилища \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="45b6d-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="45b6d-124">Содержит биометрическое шаблон и связанные данные в стандартном формате.</span><span class="sxs-lookup"><span data-stu-id="45b6d-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="45b6d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="45b6d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45b6d-126">Справочник по подключаемым модулям</span><span class="sxs-lookup"><span data-stu-id="45b6d-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="45b6d-127">Функции подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="45b6d-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="45b6d-128">**вбиокуеренгинеинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="45b6d-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="45b6d-129">**вбиокуерисенсоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="45b6d-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="45b6d-130">**вбиокуеристоражеинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="45b6d-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





