---
title: Требования к программному обеспечению для API WinSNMP
description: Приложение WinSNMP должно получить доступ к WinSNMP API через библиотеку динамической компоновки WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252746"
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



 

 

 




