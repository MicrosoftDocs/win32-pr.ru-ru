---
title: Требования к программному обеспечению для API WinSNMP
description: Приложение WinSNMP должно получить доступ к WinSNMP API через библиотеку динамической компоновки WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886074"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Требования к программному обеспечению для API WinSNMP

Приложение WinSNMP должно получить доступ к WinSNMP API через библиотеку динамической компоновки WSNMP32.DLL.

Следующие файлы необходимы для поддержки функций API WinSNMP.



| Имя файла     | Описание                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. LIB  | Библиотека WinSNMP                                                                              |
| WSNMP32.DLL  | Предоставляет WinSNMP Interface                                                                   |
| WINSNMP. Высоты    | Файл заголовка WinSNMP                                                                          |
| SNMPTRAP.EXE | Получает SNMP-ловушки и перенаправляет их в MGMTAPI.DLL, библиотеку API диспетчера Microsoft SNMP |
| SNMPAPI.DLL  | Предоставляет служебные программы SNMP                                                                      |



 

 

 




