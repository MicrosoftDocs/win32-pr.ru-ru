---
description: В таблице AppId или в таблице реестра указано, что установщик настраивает и регистрирует серверы DCOM для выполнения одной из следующих задач во время установки.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Таблица AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909108"
---
# <a name="appid-table"></a>Таблица AppId

В таблице AppId или в [таблице реестра](registry-table.md) указано, что установщик настраивает и РЕГИСТРИРУЕТ серверы DCOM для выполнения одной из следующих задач во время установки.

-   Запустите DCOM-сервер под другим идентификатором, отличным от идентификатора пользователя, который активирует сервер. Например, чтобы настроить сервер DCOM так, чтобы он всегда выполнялся как интерактивный пользователь или как предопределенный пользователь.
-   Запустите сервер DCOM как службу.
-   Настройте уровень доступа по умолчанию для DCOM Server.
-   Зарегистрируйте DCOM-сервер, чтобы он был активирован на другом компьютере.

Эта таблица обрабатывается при установке компонента, связанного с сервером DCOM, в \_ столбце Component [таблицы Class](class-table.md). Идентификатор AppId не объявлен.

Таблица AppId содержит следующие столбцы.



| Столбец               | Type                       | Ключ | Допускает значения NULL |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | Да   | Нет        |
| ремотесервернаме     | [Формате](formatted.md) | Нет   | Да        |
| локальная служба.         | [Text](text.md)           | Нет   | Да        |
| сервицепараметерс    | [Text](text.md)           | Нет   | Да        |
| дллсуррогате         | [Text](text.md)           | Нет   | Да        |
| активатеатстораже    | [Integer](integer.md)     | Нет   | Да        |
| рунасинтерактивеусер | [Integer](integer.md)     | Нет   | Да        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>ИД
</dt> <dd>

Столбец AppId [таблицы Class](class-table.md) является внешним ключом в этом столбце таблицы AppID. Этот столбец содержит значение AppId, которое будет записано в CLSID, и создает ключ GUID AppId в разделе HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>ремотесервернаме
</dt> <dd>

Этот столбец содержит значение "Ремотесервернаме" = <xxxx> , которое будет записано в разделе HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Этот столбец содержит значение LocalService, которое будет записано в разделе HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>сервицепараметерс
</dt> <dd>

Этот столбец содержит значение Сервицепараметерс, которое будет записано в разделе HKCR \\ AppID \\ {AppID>} "сервицепараметерс".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>дллсуррогате
</dt> <dd>

Этот столбец содержит значение Дллсуррогате, которое будет записано в разделе HKCR \\ AppID \\ { <appid> } "дллсуррогате" = <xxx> . Если этот столбец уже имеется, он обычно будет пустой строкой.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>активатеатстораже
</dt> <dd>

Ненулевое целочисленное значение в этом поле приводит к тому, что установщик Windows записи HKCR \\ AppID \\ { <appid> } "активатеатстораже" = "Y" в реестр. Если поле оставлено пустым или имеет нулевое значение, значение не будет записано.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>рунасинтерактивеусер
</dt> <dd>

Ненулевое целочисленное значение в этом поле приводит к тому, что установщик Windows записи HKCR \\ AppID \\ {AppID>} "runas" = "Interactive User" в реестр. Если поле оставлено пустым или имеет нулевое значение, значение не будет записано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта таблица используется действием [регистерклассинфо](registerclassinfo-action.md) и [унрегистерклассинфо](unregisterclassinfo-action.md).

Обратите внимание, что в таблице AppId нет столбца для регистрации имени по умолчанию. Поэтому в случаях, когда необходимо написать понятное имя в качестве значения имени по умолчанию, необходимо зарегистрировать его с помощью [таблицы реестра](registry-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



