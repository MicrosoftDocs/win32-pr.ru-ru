---
description: В этом разделе содержится обзор API цифровой подписи XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: О API цифровых подписей XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfbd6000df56d96afbc86a3cd0111c02a128c3c23c0d0de59717da5f4e9ac6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950944"
---
# <a name="about-xps-digital-signature-api"></a>О API цифровых подписей XPS

Документы XPS могут иметь цифровые подписи, позволяющие пользователям подписывать документ, проверять удостоверение подписавшего и указывать, изменился ли документ XPS с момента подписания. собственное Windows приложение может использовать интерфейсы API цифровой подписи XPS для выполнения операций с цифровыми подписями в документе XPS. В этом разделе содержится обзор API цифровой подписи XPS.

Интерфейс [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) управляет операциями цифровой подписи в документе XPS. Прежде чем приложение сможет получить доступ к цифровым подписям документа XPS, приложение должно вызвать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать **икспссигнатуреманажер** , а затем вызвать [**Икспссигнатуреманажер:: Лоадпаккажефиле**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) или [**ИКСПССИГНАТУРЕМАНАЖЕР:: LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) для загрузки документа XPS. Дополнительные сведения об этом процессе инициализации см. [в разделе Инициализация диспетчера подписей](initialize-the-signature-manager.md).

После загрузки документа XPS в интерфейс [**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) приложение может получить доступ к цифровым подписям документа и запросам цифровой подписи. Доступ к цифровым подписям можно получить с помощью интерфейса [**икспссигнатуре**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) в интерфейсе [**икспссигнатуреколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) диспетчера подписей. Приложение также может добавлять и удалять интерфейсы **икспссигнатуре** из коллекции. Доступ к запросам на подпись осуществляется с помощью [**икспссигнатуререкуест**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) , собираемых в интерфейсе [**икспссигнатуререкуестколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) . **Икспссигнатуререкуестколлектион** является частью интерфейса [**икспссигнатуреблокк**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) , который собираются в [**икспссигнатуреблоккколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) диспетчера сигнатур.

Приложения могут использовать [**икспссигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) диспетчера подписей для доступа к параметрам цифровой подписи и их настройки.

Примеры доступа к цифровым подписям документа XPS см. в разделе [Общие задачи программирования цифровых подписей](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование API цифровых подписей XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Справочник по API цифровых подписей XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Упаковка](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[стандартные ECMA-376, Office форматы файлов Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
