---
title: Управляемый справочник по классам команд Windows PowerShell WinRM
description: Служба удаленного управления Windows 2,0 (WinRM) может использовать командлеты Windows PowerShell для управления системой. Командлеты Windows PowerShell позволяют администратору настраивать WinRM и получать данные или управлять ресурсами.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- коннектвсманкомманд
- дисаблевсманкредсспкомманд
- дисконнектвсманкомманд
- енаблевсманкредсспкомманд
- жетвсманкредсспкомманд
- жетвсманинстанцекомманд
- инвокевсманактионкомманд
- неввсманинстанцекомманд
- неввсмансессионоптионкомманд
- ремовевсманинстанцекомманд
- сетвсманинстанцекомманд
- сетвсманкуиккконфигкомманд
- тествсманкомманд
- SessionOption
- Проверка подлинностиМеханизм
- проксякцесстипе
- проксяусентикатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd74af81c1cec7874ec0e881dbc236f5dd94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262518"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Управляемый справочник по классам команд Windows PowerShell WinRM

Служба удаленного управления Windows 2,0 (WinRM) может использовать командлеты Windows PowerShell для управления системой. Командлеты Windows PowerShell позволяют администратору настраивать WinRM и получать данные или управлять ресурсами.

Командлеты Windows PowerShell для WinRM предоставляют те же функциональные возможности, что и программа командной строки WinRM. Однако Windows PowerShell также выполняет следующие действия:

-   Автоматизирует задачи WinRM на расширяемом языке программирования, ориентированном на управление.
-   Предоставляет единый инструмент для всех задач управления.

Дополнительные сведения см. в разделе [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

## <a name="ws-management-windows-powershell-classes"></a>WS-Management классов Windows PowerShell

**Пространство имен**: Microsoft. WsMan. Management

**Сборка**: System. Management. Automation

Windows PowerShell реализует следующие классы команд WinRM. Эти классы включены в этот пакет средств разработки программного обеспечения (SDK) только для полноты. Члены этих классов не могут использоваться напрямую, и их нельзя использовать для наследования других классов.



| Класс                        | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| коннектвсманкомманд          | Подключается к службе удаленного управления Windows на удаленном компьютере. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                              |
| дисаблевсманкредсспкомманд   | Отключает проверку подлинности CredSSP на клиенте.<br/> Дополнительные сведения о параметрах и примерах см. в разделе командлет [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                           |
| дисконнектвсманкомманд       | Отключает службу WinRM на удаленном компьютере. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Disconnect-WSMan](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                      |
| енаблевсманкредсспкомманд    | Включает проверку подлинности CredSSP на клиенте.<br/> Примеры и подробные сведения о параметрах см. в описании командлета [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                               |
| жетвсманкредсспкомманд       | Возвращает конфигурацию, связанную с CredSSP для клиента.<br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                         |
| жетвсманинстанцекомманд      | Выводит сведения управления для экземпляра ресурса, указанного URI ресурса.<br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                          |
| инвокевсманактионкомманд     | Вызывает действие для целевого объекта, заданного универсальным кодом ресурса (URI) и селекторами. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                         |
| неввсманинстанцекомманд      | Создает новый экземпляр ресурса управления. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [New-WSManInstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                             |
| неввсмансессионоптионкомманд | Создает хэш-таблицу параметров сеанса WinRM для использования в качестве входных параметров для следующих командлетов WSMan: [Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true), [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true), [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)и [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Примеры и подробные сведения о параметрах см. в разделе [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/> |
| ремовевсманинстанцекомманд   | Удаляет экземпляр ресурса управления. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Remove-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                                   |
| сетвсманинстанцекомманд      | Изменяет данные управления, связанные с ресурсом. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                       |
| сетвсманкуиккконфигкомманд   | Настраивает локальный компьютер для удаленного управления. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Set-WSManQuickConfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                      |
| тествсманкомманд             | Проверяет, запущена ли служба удаленного управления Windows на локальном или удаленном компьютере. <br/> Примеры и подробные сведения о параметрах см. в разделе командлет [Test-WSMan]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Определяет набор расширенных параметров для сеанса WS-Management.<br/> Примеры и подробные сведения о возможных значениях см. в разделе командлет [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management перечислений Windows PowerShell

В Windows PowerShell реализованы следующие перечисления. Эти перечисления включены в этот пакет средств разработки программного обеспечения (SDK) только для полноты.



| Перечисление             | Описание                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Проверка подлинностиМеханизм | Задает способ проверки подлинности, используемый на сервере. <br/> Примеры и подробные сведения о возможных значениях см. в разделе командлет [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>      |
| проксякцесстипе         | Задает механизм определения расположения прокси-сервера.<br/> Примеры и подробные сведения о возможных значениях см. в разделе командлет [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/> |
| проксяусентикатион     | Задает метод аутентификации, используемый на прокси-сервере.<br/> Примеры и подробные сведения о возможных значениях см. в разделе командлет [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/>      |



 

 

