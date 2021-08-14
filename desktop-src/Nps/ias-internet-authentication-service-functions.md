---
title: Функции расширений NPS
description: Функции расширений NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cecf8ead61e94287ba4846b82f922af40068a771a9bcadd8ccb51693709c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362364"
---
# <a name="nps-extensions-functions"></a>Функции расширений NPS

> [!Note]  
> служба проверки подлинности в интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008. Содержимое этого раздела относится как к IAS, так и к NPS. По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.

 

## <a name="application-defined"></a>Определено приложением

Архитектура библиотек DLL расширения NPS поддерживает следующие экспортированные функции:

-   [**радиусекстенсионфриаттрибутес**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**радиусекстенсионинит**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**радиусекстенсионпроцесс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**радиусекстенсионпроцессекс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**радиусекстенсионтерм**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Функции [**радиусекстенсионинит**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) и [**радиусекстенсионтерм**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) являются необязательными.

Библиотека DLL расширения может экспортировать [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) вместо [**радиусекстенсионпроцесс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) или [**радиусекстенсионпроцессекс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Если библиотека DLL расширения экспортирует [**радиусекстенсионпроцессекс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), необходимо также экспортировать [**радиусекстенсионфриаттрибутес**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Определено системой

Когда сервер политики сети вызывает реализацию [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS передает функции указатель на структуру [**\_ \_ управляющего \_ блока расширения RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .

[**\_ \_ Управляющая \_ Структура расширения RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) содержит указатели на функции для следующих функций, предоставляемых NPS:

-   [**Запрос на**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**сетреспонсетипе**](/previous-versions/ms688462(v=vs.85))

[**Функции GetResponse**](/previous-versions/ms688263(v=vs.85)) и [**GetResponse**](/previous-versions/ms688270(v=vs.85)) возвращают указатели на структуру типа [**\_ \_ массива атрибутов RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

Структура [**\_ \_ массива атрибутов RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) содержит указатели на функции для следующих функций, предоставляемых NPS:

-   [**Add**](/previous-versions/ms688246(v=vs.85))
-   [**аттрибутеат**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**инсертат**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 