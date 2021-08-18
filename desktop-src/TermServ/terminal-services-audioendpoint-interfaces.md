---
title: Интерфейсы службы удаленных рабочих столов Аудиоендпоинт
description: С API Аудиоендпоинт используются следующие интерфейсы.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000074"
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

## <a name="remarks"></a>Remarks

Службы удаленных рабочих столов API Аудиоендпоинт для использования в сценариях удаленный рабочий стол; Он не предназначен для клиентских приложений.

 

 




