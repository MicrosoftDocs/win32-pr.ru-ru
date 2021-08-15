---
title: Свойство Хелпконтекстид (объект Command)
description: Сведения о свойстве Хелпконтекстид объекта Command. не рекомендуется использовать Microsoft Agent на Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38d0f725c0c809c70fa77b89d3608f8e713fd968c33bfb0192c712f3613e91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478711"
---
# <a name="helpcontextid-property-command-object"></a>Свойство Хелпконтекстид (объект Command)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

если вы создали файл справки Windows для приложения и присвойте файлу свойство [**HelpFile**](helpfile-property.md) в файле, агент автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **True** и пользователь выбирает команду. Если задать номер контекста в [**хелпконтекстид**](helpcontextid-property.md), агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

> [!Note]  
> для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**HelpFile, свойство**](helpfile-property.md)


 

 
