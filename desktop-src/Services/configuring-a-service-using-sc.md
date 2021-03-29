---
description: Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для запроса или изменения базы данных установленных служб. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Настройка службы с помощью SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662254"
---
# <a name="configuring-a-service-using-sc"></a>Настройка службы с помощью SC

Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для запроса или изменения базы данных установленных служб. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.

## <a name="syntax"></a>Синтаксис

**SC** \[ *Имя сервера* \] *Команда* \[  \] ServiceName \[  \] параметр1 \[ *параметр2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Имя*
</dt> <dd>

Необязательное имя сервера. Используйте форму \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Кнопки*
</dt> <dd>

Одна из следующих команд:

<dl> <dd>boot</dd> <dd>config</dd> <dd>create</dd> <dd>удалить</dd> <dd>description;</dd> <dd>енумдепенд</dd> <dd>ошибка</dd> <dd>фаилурефлаг</dd> <dd>Переdisplayname</dd> <dd>жеткэйнаме</dd> <dd>Блокировка</dd> <dd>qc</dd> <dd>кдескриптион</dd> <dd>кфаилуре</dd> <dd>кфаилурефлаг</dd> <dd>кпривс</dd> <dd>ксидтипе</dd> <dd>query</dd> <dd>QueryEx</dd> <dd>привс</dd> <dd>куерилокк</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>Идентификатор типа безопасности</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Служба*
</dt> <dd>

Имя службы, указанное при ее установке.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*параметр1*
</dt> <dd>

Необязательный параметр.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*вариант 2*
</dt> <dd>

Необязательный параметр.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы просмотреть полный синтаксис команды, используйте следующую команду:

 *команда* SC

## <a name="related-topics"></a>См. также

<dl> <dt>

[Конфигурация службы](service-configuration.md)
</dt> <dt>

[Установка, удаление и перечисление служб](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



