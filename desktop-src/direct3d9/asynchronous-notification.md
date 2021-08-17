---
description: Существует ряд интересных запросов к драйверу, который может быть создан приложением в случае отсутствия затрат на производительность.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Асинхронное уведомление (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd23a64e613bbbae56154dc35c05bcf08b75c4c91f306360153e775e12c40ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123421"
---
# <a name="asynchronous-notification-direct3d-9"></a>Асинхронное уведомление (Direct3D 9)

Существует ряд интересных запросов к драйверу, который может быть создан приложением в случае отсутствия затрат на производительность. В Direct3D 7 и Direct3D 8 механизм синхронных запросов, а также очень хорошо работал для таких целей, как статистика, но не были добавлены критически важные для производительности запросы. Существуют и другие вещи (например, ограждения), которые по сути являются асинхронными. Это простой API для выполнения как синхронных, так и асинхронных запросов. Сведения будут сняты с учета в Direct3D 9.

Создайте запрос с помощью [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api). Этот метод принимает D3DQUERYTYPE, который определяет, какой тип запроса необходимо сделать, и возвращает указатель на объект [**IDirect3DQuery9**](/windows/desktop/api) . Если тип запроса не поддерживается, вызов возвращает ошибку D3DERR \_ NOTAVAILABLE. С помощью объекта Query приложение отправляет запрос в среду выполнения с помощью [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)и опрашивает состояние запроса с помощью [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Если результат запроса доступен, \_ возвращается s OK; в противном случае \_ возвращается значение s false. Предполагается, что приложение передает буфер соответствующего размера для результатов запроса.

Приложение может заставить среду выполнения принудительно сбрасывать запрос к драйверу с помощью D3DGETDATA \_ flush с [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Она вызывает сброс, вызывая драйвер для просмотра запроса. В этом случае D3DERR \_ девицелост возвращается, если устройство будет потеряно.

При потере устройства все запросы теряются, поэтому приложение должно их повторно создать. Если устройство не поддерживает запрос и Пкуерид имеет **значение NULL**, создание запроса завершится ошибкой с помощью D3DERR \_ инвалидкалл.

В следующей таблице приведены важные сведения о каждом типе запроса.



| куертитипе                    | Допустимый флаг проблемы              | Буфер GetData              | Среда выполнения      | Неявное начало запроса |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ вкаче          | D3DISSUE \_ конец                 | D3DDEVINFO \_ вкаче          | Розничная или отладочная | креатедевице                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ конец                 | D3DDEVINFO \_ ResourceManager | Только Отладка   | Присутствует                     |
| D3DQUERYTYPE \_ вертексстатс     | D3DISSUE \_ конец                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Только Отладка   | Присутствует                     |
| \_Событие D3DQUERYTYPE           | D3DISSUE \_ конец                 | BOOL                        | Розничная или отладочная | креатедевице                |
| D3DQUERYTYPE \_ перекрытия       | \_Начало D3DISSUE, D3DISSUE \_ конец | DWORD                       | Розничная или отладочная | Н/Д                         |



 

Поле флагов для [**IDirect3DQuery9:: дата_выпуска**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Поле Flags для [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Советы программирования](programming-tips.md)
</dt> </dl>

 

 
