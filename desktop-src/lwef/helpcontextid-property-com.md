---
title: Свойство Хелпконтекстид (объект Command)
description: Сведения о свойстве Хелпконтекстид объекта Command. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068518"
---
# <a name="helpcontextid-property-command-object"></a>Свойство Хелпконтекстид (объект Command)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает связанный контекстный номер для объекта [**команды**](/windows/desktop/lwef/the-command-object) . Используется для предоставления контекстной справки для объекта **Command** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Команды ("")._ *  \[  =  *Номер* хелпконтекстид\]



| Часть     | Описание                                   |
|----------|-----------------------------------------------|
| *Число* | Целое число, указывающее допустимый контекстный номер. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Если вы создали файл справки Windows для приложения и присвойте файлу свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду. Если задать номер контекста в [**хелпконтекстид**](helpcontextid-property.md), агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

> [!Note]  
> Для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**HelpFile, свойство**](helpfile-property.md)


 

 
