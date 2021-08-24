---
title: Сообщение TVM_GETNEXTITEM (Коммктрл. h)
description: Извлекает элемент представления дерева, который несет указанную связь с указанным элементом. Это сообщение можно отправить явно с помощью \_ макроса Жетнекститем TreeView.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- элементы управления Windows сообщений TVM_GETNEXTITEM
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698684"
---
# <a name="tvm_getnextitem-message"></a>\_Сообщение TVM жетнекститем

Извлекает элемент представления дерева, который несет указанную связь с указанным элементом. Это сообщение можно отправить явно с помощью макроса [**\_ жетнекститем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг, указывающий элемент для извлечения. Этот параметр может принимать одно из следующих значений:



| Значение                                                                                                                                                                              | Значение                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**ТВГН \_ курсор**</dt> </dl>                               | Извлекает выбранный в данный момент элемент. Для отправки этого сообщения можно использовать макрос " [**\_ выделять**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) " в TreeView.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**\_дочерний элемент твгн**</dt> </dl>                               | Извлекает первый дочерний элемент элемента, указанного параметром *хитем* . Вы можете отправить это сообщение с помощью макроса [**\_ дочернего элемента TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) .<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**ТВГН \_ дрофилите**</dt> </dl>                | Извлекает элемент, являющийся целью операции перетаскивания. Для отправки этого сообщения можно использовать макрос [**\_ жетдрофилигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) .<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**ТВГН \_ фирствисибле**</dt> </dl>          | Извлекает первый элемент, видимый в окне древовидного представления. Для отправки этого сообщения можно использовать макрос [**\_ жетфирствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) .<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**ТВГН \_ ластвисибле**</dt> </dl>             | [Версия 4,71](common-control-versions.md). Извлекает последний развернутый элемент в дереве. При этом последний элемент, видимый в окне древовидного представления, не извлекается. Для отправки этого сообщения можно использовать макрос [**\_ жетластвисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) .<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**ТВГН \_ Далее**</dt> </dl>                                  | Извлекает следующий элемент того же уровня. Для отправки этого сообщения можно использовать макрос [**\_ жетнекстсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) .<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**ТВГН \_ некстселектед**</dt> </dl>          | **Windows Vista и более поздних версий.** Извлекает следующий выбранный элемент. Для отправки этого сообщения можно использовать макрос [**\_ жетнекстселектед TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) .<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**ТВГН \_ некствисибле**</dt> </dl>             | Извлекает следующий видимый элемент, следующий за указанным элементом. Указанный элемент должен быть видимым. Используйте сообщение [**TVM \_ жетитемрект**](tvm-getitemrect.md) , чтобы определить, является ли элемент видимым. Для отправки этого сообщения можно использовать макрос [**\_ жетнекствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) .<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**\_родительский твгн**</dt> </dl>                            | Возвращает родительский элемент указанного элемента. Для отправки этого сообщения можно использовать макрос « [**\_ родители**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) ».<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**ТВГН \_ назад**</dt> </dl>                      | Извлекает предыдущий элемент того же уровня. Для отправки этого сообщения можно использовать макрос [**\_ жетпревсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) .<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**ТВГН \_ превиаусвисибле**</dt> </dl> | Извлекает первый видимый элемент, предшествующий указанному элементу. Указанный элемент должен быть видимым. Используйте сообщение [**TVM \_ жетитемрект**](tvm-getitemrect.md) , чтобы определить, является ли элемент видимым. Для отправки этого сообщения можно использовать макрос [**\_ жетпреввисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) .<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**\_корневой твгн**</dt> </dl>                                  | Извлекает верхний или самый первый элемент элемента управления "дерево-представление". Для отправки этого сообщения можно использовать макрос " [**\_ root**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) ". <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер элемента, если он успешно выполнен. В большинстве случаев сообщение возвращает значение **null** , указывающее на ошибку. Подробные сведения см. в разделе "Заметки".

## <a name="remarks"></a>Remarks

Это сообщение будет возвращать **значение NULL** , если извлекаемый элемент является корневым узлом дерева. Например, если вы используете это сообщение с \_ родительским флагом твгн в дочернем элементе первого уровня корневого узла древовидного представления, сообщение вернет **значение NULL**.

Можно также использовать один из следующих связанных макросов:



|                                                               |
|---------------------------------------------------------------|
| [**Элемент управления TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**\_Жетдрофилигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**\_Жетфирствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**\_Жетластвисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**\_Жетнекстсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**\_Жетнекствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**\_Родители TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**\_Жетпревсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**\_Жетпреввисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**\_Корень TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**\_Выбор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





