---
description: Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для управления службой. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Управление службой с помощью SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664201"
---
# <a name="controlling-a-service-using-sc"></a>Управление службой с помощью SC

Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для управления службой. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.

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

<dl> <dd>continue</dd> <dd>управляющие</dd> <dd>запросить</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

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

[Запросы управления службами](service-control-requests.md)
</dt> <dt>

[Запуск службы](service-startup.md)
</dt> </dl>

 

 



