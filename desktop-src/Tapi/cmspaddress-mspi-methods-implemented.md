---
description: Ниже приведены стандартные методы МСПИ, которые должны быть реализованы всеми MSP. Основная документация по этим методам существует в разделе справочника по интерфейсу поставщика услуг мультимедиа (МСПИ).
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: Реализованные методы МСПИ Кмспаддресс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed19bbacc13990d052c35bda68f97db80ff68ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684321"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>Реализованные методы МСПИ Кмспаддресс

Ниже приведены стандартные методы МСПИ, которые должны быть реализованы всеми MSP. Основная документация по этим методам существует в разделе [справочника по интерфейсу поставщика услуг мультимедиа (мспи)](media-service-provider-interface-mspi-reference.md) .



| Методы Кмспаддресс                                                                          | Описание                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Инициализация**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | (Интерфейс [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Вызывается методом TAPI3 при первом создании этого MSP.                                                                                                                                                                                                                                                                                                   |
| [**Закрытия**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | (Интерфейс [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Вызывается методом TAPI3, если этот адрес больше не используется.                                                                                                                                                                                                                                                                                         |
| [**рецеиветспдата**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | (Интерфейс [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Вызывается методом TAPI3, когда TSP отправляет данные в этот объект адреса MSP.                                                                                                                                                                                                                                                                               |
| [**Четный**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    | (Интерфейс [**итмспаддресс**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Вызывается методом TAPI3 для получения подробных сведений о событии.                                                                                                                                                                                                                                                                                       |
| [**получить \_ статиктерминалс**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Оболочка OLE-автоматизации для вспомогательной функции [**жетстатиктерминалс**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                            |
| [**енумератестатиктерминалс**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Оболочка перечисления для вспомогательной функции [**жетстатиктерминалс**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                               |
| [**получить \_ динамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Оболочка OLE-автоматизации для вспомогательной функции [**жетдинамиктерминалклассес**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                              |
| [**енумератединамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Оболочка перечисления для вспомогательной функции [**жетдинамиктерминалклассес**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                                 |
| [**креатетерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Этот метод вызывается приложением для создания динамического терминала. Он планирует рабочий элемент в рабочем потоке MSP, который во время выполнения запрашивает у диспетчера терминалов создание динамического терминала. Производный класс может переопределять этот метод, чтобы иметь собственный способ создания динамического терминала.                                |
| [**жетдефаултстатиктерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               | (Интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Этот метод вызывается приложением для получения статического терминала по умолчанию для указанного типа и направления. Он обновляет список терминалов по умолчанию (при необходимости) и возвращает указатель интерфейса. Производный класс может переопределить этот метод, чтобы он мог определить, какой терминал является значением по умолчанию. Блокирует списки терминалов. |



 

 

 
