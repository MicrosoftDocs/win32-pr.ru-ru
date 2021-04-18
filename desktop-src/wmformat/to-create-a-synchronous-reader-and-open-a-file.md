---
title: Создание синхронного средства чтения и открытие файла
description: Создание синхронного средства чтения и открытие файла
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Расширенный системный формат (ASF), создание читателей
- ASF (Расширенный системный формат), создание читателей
- Расширенный формат систем (ASF), открытие файлов
- ASF (Расширенный системный формат), открытие файлов
- синхронные читатели, создание
- синхронные читатели, открытие файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700823"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Создание синхронного средства чтения и открытие файла

Прежде чем выполнять какие-либо действия с синхронным модулем чтения, необходимо создать синхронный объект Reader и загрузить файл для чтения. Чтобы инициализировать синхронное средство чтения и открыть файл, выполните следующие действия.

1.  Создайте синхронный объект Reader, вызвав функцию [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) . Необходимо указать требуемый уровень Rights Management для нового объекта модуля чтения. Доступные режимы перечислены в типе перечисления **\_ Rights ВМТ** .
2.  Укажите файл для чтения путем вызова [**ивмсинкреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

Синхронное средство чтения также поддерживает использование интерфейса **IStream** com для открытия файлов. Интерфейс **IStream** можно реализовать любым выбранным способом. После открытия требуемого файла в **IStream** можно выполнить приведенные выше действия, за исключением того, что необходимо вызвать [**Ивмсинкреадер:: опенстреам**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) вместо **ивмсинкреадер:: Open** на шаге 2.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Чтение файлов с помощью синхронного модуля чтения**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




