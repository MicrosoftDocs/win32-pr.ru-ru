---
description: Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для управления службой. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Управление службой с помощью SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126454"
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

<dl> <dd>continue</dd> <dd>управляющие</dd> <dd>запросить</dd> <dd>pause</dd> <dd>запуск</dd> <dd>stop</dd> </dl> </dd> <dt>

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

## <a name="remarks"></a>Remarks

Чтобы просмотреть полный синтаксис команды, используйте следующую команду:

 *команда* SC

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запросы управления службами](service-control-requests.md)
</dt> <dt>

[Запуск службы](service-startup.md)
</dt> </dl>

 

 



