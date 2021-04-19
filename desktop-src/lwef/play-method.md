---
title: Метод Play (устаревшие функции среды Windows)
description: Метод Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691722"
---
# <a name="play-method-legacy-windows-environment-features"></a>Метод Play (устаревшие функции среды Windows)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Воспроизводит указанную анимацию для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Воспроизвести_* "*аниматионнаме*"

</dd> </dl> 

| Отделение            | Описание                                                          |
|-----------------|----------------------------------------------------------------------|
| *аниматионнаме* | Обязательный. Строка, указывающая имя последовательности анимации. |



 

## <a name="remarks"></a>Комментарии

Имя анимации определяется при компиляции символа с помощью редактора символов Microsoft Agent. Прежде чем воспроизводить указанную анимацию, сервер пытается воспроизвести анимацию **возврата** для предыдущей анимации, если она была назначена.

При доступе к анимации символа с помощью обычного файлового протокола можно просто использовать метод **Play** , указывающий имя анимации. Однако при использовании протокола HTTP для доступа к данным анимации символов используйте метод **Get** для загрузки анимации перед вызовом метода **Play** .

Дополнительные сведения см. в описании метода **Get** .

Чтобы упростить синтаксис, можно объявить ссылку на объект и задать для него ссылку на [**символьный**](/windows/desktop/lwef/the-characters-object) объект в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) и использовать ссылку как часть операторов **Play** :


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) . Кроме того, если вы укажете незагруженную анимацию или не удалось загрузить символ, сервер устанавливает свойство [**Status**](status-property.md) объекта **запроса** в значение "Failed" с соответствующим номером ошибки. Однако если анимация не существует и данные этого символа уже были успешно загружены, сервер вызывает ошибку.

Метод **Play** не делает символ видимым. Если символ не виден, сервер воспроизводит анимацию незаметно и задает свойство [**Status**](status-property.md) объекта [**request**](/windows/desktop/lwef/the-request-object) .

 

 
