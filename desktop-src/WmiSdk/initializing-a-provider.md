---
description: Одна из первых задач, которую необходимо запрограммировать для поставщика, — это процесс инициализации, который охватывает все задачи, которые должен выполнить поставщик, что позволяет ему отправлять и получать данные из WMI, управлять управляемым объектом и выполнять другие задачи.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Инициализация поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e373cf72d4715919a9d7fc59064d156e80a1f2371c585d698a7c6edff4f22fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097284"
---
# <a name="initializing-a-provider"></a>Инициализация поставщика

Одна из первых задач, которую необходимо запрограммировать для поставщика, — это процесс инициализации, который охватывает все задачи, которые должен выполнить поставщик, что позволяет ему отправлять и получать данные из WMI, управлять управляемым объектом и выполнять другие задачи. Каждый тип поставщика имеет свой набор задач, который должен выполняться и имеет сопутствующий набор уникальных интерфейсов.

Однако все поставщики инициализируются через интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и СООБЩАют инструментарию WMI о своем состоянии инициализации через интерфейс [**ивбемпровидеринитсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .

В следующей процедуре описывается инициализация поставщика.

**Инициализация поставщика**

1.  Реализуйте [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) для поставщика.

    Когда WMI определяет, что клиенту требуются службы поставщика, WMI загружает поставщик, вызывая метод [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Реализуйте любые интерфейсы, уникальные для вашего типа поставщика.
3.  Сообщите инструментарию WMI о том, что поставщик завершен с инициализацией, вызвав [**ивбемпровидеринитсинк:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Все реализации [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) должны вызывать [**Ивбемпровидеринитсинк:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) для передачи состояния инициализации в WMI. Метод **SetStatus** позволяет инструментарию WMI определить, готов ли поставщик к получению запросов, и тип запросов, которые поставщик готов к получению.

Следующая процедура описывает, как сообщить об успешной инициализации.

**Чтобы сообщить об успешной инициализации**

-   Установите для параметра *Истатус* [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) значение **WBEM, \_ \_ инициализированное**.

    После того как вы вернете значение **WBEM \_ \_**, поставщик указывает на готовность к обработке запросов от приложений, WMI и других поставщиков. После инициализации WBEM \_ \_ , Инструментарий WMI выполняет вызов метода [**Ивбемпровидеринит:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) поставщика. Этот запрос получает указатель на основной интерфейс поставщика.

Следующая процедура описывает, как сообщить об ошибке во время инициализации.

**Сообщение об ошибке во время инициализации**

-   Установите для параметра *Истатус* [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) значение **WBEM \_ E \_ не удалось**. Поставщики представлений WMI, которые возвращают **WBEM \_ E \_** , не работают.

    Инструментарий WMI освобождает указатель [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) либо после того, как WMI получил указатель на основной интерфейс поставщика или после сбоя инициализации.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка поставщика WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Защита поставщика](securing-your-provider.md)
</dt> </dl>

 

 



