#React Native

##布局总结：
1. 父视图属性(容器属性)：
	2. ***`flexDirection(属性定义了父视图中的子元素沿横轴或侧轴方片的排列方式。)`*** enum(`row`, `column`,`row-reverse`,`column-reverse`)
	3. ***`flexWrap(属性定义了子元素在父视图内是否允许多行排列，默认为nowrap。)`*** enum(`wrap`, `nowrap`)
	4. ***`justifyContent(父容器主轴的弹性)`*** enum(`flex-start`, `flex-end`, `center`, `space-between`, `space-around`)
	5. ***`alignItems(侧轴方向)`*** enum(`flex-start`, `flex-end`, `center`, `stretch`)
6. 子视图属性
	7. ***`alignSelf`*** enum(‘auto’, ‘flex-start’, ‘flex-end’, ‘center’, ‘stretch’)
	8. ***`flex`*** number
9. 其他布局
	10. 视图边框
		11. borderBottomWidth number 底部边框宽度
		12. borderLeftWidth number 左边框宽度
		13. borderRightWidth number 右边框宽度
		14. borderTopWidth number 顶部边框宽度
		15. borderWidth number 边框宽度
		16. border<Bottom	Left	Right	Top>Color 个方向边框的颜色
		17. borderColor 边框颜色
	18. 尺寸
		19. width number
		20. height number
	21. 外边距
		22. margin number 外边距
		23. marginBottom number 下外边距
		24. marginHorizontal number 左右外边距
		25. marginLeft number 左外边距
		26. marginRight number 右外边距
		27. marginTop number 上外边距
		28. marginVertical number 上下外边距
	29. 内边距
		30. padding number 内边距
		31. paddingBottom number 下内边距
		32. paddingHorizontal number 左右内边距
		33. paddingLeft number 做内边距
		34. paddingRight number 右内边距
		35. paddingTop number 上内边距
		36. paddingVertical number 上下内边距
	37. 边缘
		38. left number 属性规定元素的左边缘。该属性定义了定位元素左外边距边界与其包含块左边界之间的偏移。
		39. right number 属性规定元素的右边缘。该属性定义了定位元素右外边距边界与其包含块右边界之间的偏移
		40. top number 属性规定元素的顶部边缘。该属性定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。
		41. bottom number 属性规定元素的底部边缘。该属性定义了一个定位元素的下外边距边界与其包含块下边界之间的偏移。
	42. 层次
		43. zIndex：zIndex值越大，渲染的时候就越在顶部！

	

