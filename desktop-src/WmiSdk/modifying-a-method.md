---
description: Помимо классов и экземпляров, Инструментарий WMI позволяет изменять метод. Основной причиной, по которой необходимо изменить метод, является изменение реализации метода в поставщике. Дополнительные сведения см. в разделе Написание поставщика методов.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Изменение метода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423597"
---
# <a name="modifying-a-method"></a>Изменение метода

Помимо классов и экземпляров, Инструментарий WMI позволяет изменять метод. Основной причиной, по которой необходимо изменить метод, является изменение реализации метода в поставщике. Дополнительные сведения см. [в разделе Написание поставщика методов](writing-a-method-provider.md).

Изменение метода не является операцией, которая может быть выполнена в скрипте.

Следующая процедура описывает, как изменить метод программным способом.

**Изменение метода программным способом**

1.  Получите определение класса с помощью вызова [**метода ивбемклассобжект::-Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    Два выходных параметра, *ппинсигнатуре* и *ппаутсигнатуре*, содержат класс в параметре и класс out-Parameter соответственно. Возвращаемое значение объединяется в класс параметра out в качестве свойства и должно называться **ReturnValue**.

2.  Извлеките и измените параметры с помощью вызовов [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)или [**ивбемклассобжект::D удалить**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Поместите новую версию метода обратно в родительский класс с помощью вызова [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

 

 



