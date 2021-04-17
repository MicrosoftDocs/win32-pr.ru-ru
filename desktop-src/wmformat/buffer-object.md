---
title: Объект buffer
description: Объект buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, буферные объекты
- Расширенный системный формат (ASF), буферные объекты
- ASF (Расширенный системный формат), объекты buffer
- объекты, объекты buffer
- Объекты буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105700817"
---
# <a name="buffer-object"></a>Объект buffer

Объект buffer используется для хранения образцов и их доставки между объектами пакета SDK Windows Media Format и приложением. При написании файла входные образцы передаются в модуль записи с помощью объектов buffer. При чтении файла объект Reader или синхронный объект Reader предоставляет примеры для приложения в объектах буфера.

Для записи образцов в файл можно создать объект buffer с помощью метода [**ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) . Для чтения образцов объект Reader и синхронный объект Reader создают объекты буфера внутренним образом. При выборе вы можете выделить собственные объекты буфера для чтения файлов с помощью [**ивмреадераллокаторекс:: аллокатефораутпутекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) или [**Ивмреадераллокаторекс:: аллокатефорстреамекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).

Каждый объект buffer поддерживает следующие интерфейсы.



| Интерфейс                          | Описание                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**инссбуффер**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Элементы управления и предоставляют доступ к буферу.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Не реализован.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Поддерживает свойства буфера, используемые для расширений модулей данных. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Перечисляет свойства буфера.                                        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объекты**](objects.md)
</dt> </dl>

 

 




