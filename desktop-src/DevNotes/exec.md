---
description: HKLM \\ программное обеспечение \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807720"
---
# <a name="exec"></a>Exec

**HKLM \\ программное обеспечение \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Тип данных | Диапазон                    | Значение по умолчанию |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *Путь к исполняемому файлу* |               |



 

## <a name="browser-integration-steps"></a>Шаги интеграции с браузером

1.  Используйте функцию [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) , чтобы определить, установлена ли диагностика сети. Если он установлен, будет указан ключ **{e2e2dd38-d088-4134-82b7-f2ba38496583}** .
2.  Используйте функцию [**процедура RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) , чтобы получить путь к исполняемому файлу диагностики сети из записи **exec** .
3.  Отобразить новую страницу ошибки, если она установлена в системе.
4.  Создайте расширение браузера, которое создает стандартный элемент панели инструментов, если в системе установлен модуль диагностики.
5.  Запустите исполняемый файл диагностики сети, используя путь, полученный на шаге 2.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обзор функций средств диагностики сети](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
