---
description: 'Оператор вычитания класса Вбемтиме (&\# 8211;) был перегружен в:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Операторы Вбемтиме:: operator-(Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713026"
---
# <a name="wbemtimeoperator--operators"></a>Операторы Вбемтиме:: operator-

\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Оператор вычитания класса [**вбемтиме**](wbemtime.md) () перегружен до:

-   Вычитание интервала времени из времени объекта для создания нового объекта времени, содержащего результирующее время.
-   Вычтите время из времени объекта, чтобы создать новый объект интервала времени, содержащий разницу между двумя значениями времени.

### <a name="overload-list"></a>Список перегрузок



| Оператор                                                                         | Описание                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operator — (Вбемтиме&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Вычитает **вбемтиме** из **вбемтиме**.<br/>                         |
| [**operator — (Вбемтимеспан&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Вычитает [**вбемтимеспан**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) из **вбемтиме**.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Вбемтиме. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
