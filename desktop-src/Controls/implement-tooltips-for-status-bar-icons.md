---
title: Как реализовать подсказки для значков строки состояния
description: Неагрессивный способ отобразить пояснительное сообщение для значка строки состояния — реализовать подсказку. При щелчке всплывающая подсказка исчезает, но можно также указать значение времени ожидания.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488361"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Как реализовать подсказки для значков строки состояния

Неагрессивный способ отобразить пояснительное сообщение для значка строки состояния — реализовать подсказку. При щелчке всплывающая подсказка исчезает, но можно также указать значение времени ожидания.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="implement-tooltips-for-status-bar-icons"></a>Реализация подсказок для значков строки состояния

В следующем фрагменте кода показано, как добавить всплывающую подсказку к значку строки состояния.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Комментарии

Подробное описание строки состояния см. [на панели задач](/windows/desktop/shell/taskbar).

Чтобы отобразить всплывающую подсказку, необходимо установить \_ флаг сведений о nЕсли в структуре [**нотификондата**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) и использовать члены **сзинфо** и **утимеаут** для указания текста подсказки и времени ожидания.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 