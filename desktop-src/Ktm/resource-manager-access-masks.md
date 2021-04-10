---
description: KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера ресурсов.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Маски доступа диспетчер ресурсов (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156363"
---
# <a name="resource-manager-access-masks"></a>Маски доступа диспетчер ресурсов

KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера ресурсов.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_ \_ сведения о запросе RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект может запрашивать сведения об Resource Manager (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_сведения о наборе RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Вызывающий объект может задать сведения об RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**\_Восстановление RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект может восстановить указанное RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**Прикрепление RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



Вызывающий объект может прикрепить RM в транзакции.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_ \_ уведомление о получении RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект может получить уведомление для RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_универсальное \_ Чтение RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект имеет следующие привилегии: стандартные \_ права на \_ Чтение \_ , \_ сведения о запросе ResourceManager и \_ Восстановление ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_Универсальная \_ запись RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект имеет следующие привилегии: \_ запись стандартных прав \_ , \_ сведения о наборе ResourceManager, \_ \_ Прикрепление RESOURCEMANAGER и \_ \_ уведомление о получении ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_универсальный \_ Запуск RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



Вызывающий объект имеет следующие привилегии: \_ выполнение стандартных прав \_ , \_ Прикрепление диспетчера ресурсов \_ и \_ уведомление о получении ResourceManager.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_все \_ доступ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



У вызывающего объекта есть следующие права: \_ требуются стандартные права \_ .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>Файл WinNT. h</dt> </dl> |



 

 




