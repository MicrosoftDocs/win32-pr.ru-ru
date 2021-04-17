---
title: Интерфейсы службы удаленных рабочих столов Аудиоендпоинт
description: С API Аудиоендпоинт используются следующие интерфейсы.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681414"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Интерфейсы службы удаленных рабочих столов Аудиоендпоинт

С API Аудиоендпоинт используются следующие интерфейсы.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**иаудиодевицеендпоинт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Инициализирует объект конечной точки устройства и получает возможности устройства, которое оно представляет.

</dd> <dt>

[**иаудиоендпоинт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Предоставляет сведения для обработчика аудио о конечной точке аудио. Этот интерфейс реализуется конечной точкой аудио.

</dd> <dt>

[**иаудиоендпоинтконтрол**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Управляет состоянием потока конечной точки.

</dd> <dt>

[**иаудиоендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Возвращает разницу между текущими позициями чтения и записи в буфере конечной точки.

</dd> <dt>

[**иаудиоинпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Возвращает входной буфер для каждого прохода обработки.

</dd> <dt>

[**иаудиуутпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Возвращает выходной буфер для каждого прохода обработки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Службы удаленных рабочих столов API Аудиоендпоинт для использования в сценариях удаленный рабочий стол; Он не предназначен для клиентских приложений.

 

 




