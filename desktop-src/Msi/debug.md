---
description: Если для этой системной политики на уровне компьютера задано значение &\# 0034; 1&\# 0034;, установщик записывает в отладчик общие сообщения отладки с помощью функции OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Отладка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692874"
---
# <a name="debug"></a>Отладка

Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение "1", установщик записывает в отладчик общие сообщения отладки с помощью функции [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Если это значение равно 2, установщик записывает все допустимые сообщения отладки в отладчик с помощью функции [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . эта политика предназначена только для отладки и может не поддерживаться в будущих версиях установщик Windows.

Windows Установщик записывает командные строки только в файл журнала, если в значении политики отладки задан третий бит (0x04). Таким образом, чтобы отобразить командные строки в журнале, задайте для параметра политики отладки значение 7. При этом не отображаются свойства, связанные с [элементом управления](edit-control.md) "поле ввода", имеющим [атрибут элемента управления Password](password-control-attribute.md). Это сделает свойства, заданные в командной строке, видимыми в журнале, даже если свойство включено в свойство [**мсихидденпропертиес**](msihiddenproperties.md) . Дополнительные сведения см. в разделе [предотвращение записи конфиденциальной информации в файл журнала](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Ключ реестра

**HKey \_ \_** \\ **политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows

## <a name="data-type"></a>Тип данных

**REG \_ DWORD**

 

 
